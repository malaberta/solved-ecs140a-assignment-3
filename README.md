Download Link: https://assignmentchef.com/product/solved-ecs140a-assignment-3
<br>
For each of the following problems, you are to provide two solutions:  one using the pattern-matching techniques discussed in Episode 18, and one not using those pattern-matching techniques (i.e., the ones we discussed before talking about pattern-matching over lists).  For example, the two solutions for myappend might look like:

— without pattern matching   myappend list1 list2

| list1 == [] = list2

| otherwise   = (head list1):(myappend (tail list1) list2)

— with pattern matching   myappend_pm [] list2     = list2

myappend_pm (x:xs) list2 = x:(myappend_pm xs list2)

Note that I have ended the name of the pattern-matching solution with “_pm”.  Please do the same for all the pattern-matching solutions that you submit for this assignment.

To implement the functions below, you may use only the following list operations — ‘:’, ‘head’, ‘tail’, ‘null’, and ‘elem’ . (Note that there are pattern matching equivalents for most of these.)  Do not resort to just giving a new name to an existing Haskell function that already does what we want your function to

do.  So, for example

myappend inlist1 inlist2 = inlist1 ++ inlist2

wouldn’t get you any points.

Please make sure you name your functions with the names provided below (with and without the _pm suffix).  Also, include type declarations with your functions.  It will be good practice.

1)  myremoveduplicates

myremoveduplicates “abacad” =&gt; “bcad” myremoveduplicates [3,2,1,3,2,2,1,1] =&gt; [3,2,1]

2)  myintersection

For this function, the order of the elements in the list returned by the function doesn’t matter.  Also, if the arguments to the function have duplicate elements in the list, then the result of the intersection is unspecified.

myintersection “abc” “bcd” =&gt; “bc” myintersection [3,4,2,1] [5,4,1,6,2] =&gt; [4,2,1] myintersection [] [1,2,3] =&gt; [] myintersection “abc” “” =&gt; “”

3)  mynthtail

mynthtail 0 “abcd” =&gt; “abcd” mynthtail 1 “abcd” =&gt; “bcd” mynthtail 2 “abcd” =&gt; “cd” mynthtail 3 “abcd” =&gt; “d” mynthtail 4 “abcd” =&gt; “” mynthtail 2 [1, 2, 3, 4] =&gt; [3,4] mynthtail 4 [1, 2, 3, 4] =&gt; []

4)  mylast

mylast “” =&gt; “” mylast “b” =&gt; “b” mylast “abcd” =&gt; “d” mylast [1, 2, 3, 4] =&gt; [4]

mylast [] =&gt; []

5)  myreverse

There’s a simple but inefficient solution to this problem, and a much more efficient solution.  For full credit, provide the more efficient solution.

myreverse “” =&gt; “” myreverse “abc” =&gt; “cba” myreverse [1, 2, 3] =&gt; [3, 2, 1]

myreverse [] =&gt; []

6)  myreplaceall

myreplaceall 3 7 [7,0,7,1,7,2,7] =&gt; [3,0,3,1,3,2,3]

myreplaceall ‘x’ ‘a’ “” =&gt; “”

myreplaceall ‘x’ ‘a’ “abacad” =&gt; “xbxcxd”

7)  myordered

myordered [] =&gt; True myordered [1] =&gt; True myordered [1,2] =&gt; True myordered [1,1] =&gt; True myordered [2,1] =&gt; False myordered “abcdefg” =&gt; True myordered “ba” =&gt; False