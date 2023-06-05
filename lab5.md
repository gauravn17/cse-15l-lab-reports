Lab Report 5
1. Student EdStem Question
What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?

Visual Studio Code & JUnit

Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.

I am trying to debug the ListExamples.java file, and there are failures in the testMerge1 and testMerge2 tests. Here is the symptom:





I expected to see the two lists merge in order, but I seem to be merging them in reverse order.

Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.



I can also use bash test.sh to compile and run these tests, but I'm not using Linux right now.

2. Initial TA Response
May I see what your merge method looks like so I can get a better idea of where the bug might be? Make sure you update the index variables correctly and within their respective list loops (e.g. index1 in list1 loop and index2 in list2 loop).

3. Additional Information From Student
Here is the merge method. The while loops and index variables seem to be correct.



4. Final TA Response
File & directory structure needed

1

Contents of each file before fixing the bug







Full command line(s) ran to trigger the bug
