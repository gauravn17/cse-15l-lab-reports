# Lab Report 5

## 1. Student EdStem Question

**What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?**

Visual Studio Code & JUnit

**Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.

I am trying to debug the ListExamples.java file, and there are failures in the testMerge1 and testMerge2 tests. Here is the symptom:

![image](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/769d3a33-a212-4b7b-8162-deeeee34f46d)

![image](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/43725159-ffb8-4d01-ad9f-2a4d1a9b3131)

I expected to see the two lists merge in order, but instead, they seem to be getting merged in reverse order.

**Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.

I can also use bash test.sh to compile and run these tests, but I'm not using Linux right now.

## 2. Initial TA Response

May I see what your merge method looks like so I can get a better idea of where the bug might be? Make sure you update the index variables correctly and within their respective list loops (e.g. index1 in list1 loop and index2 in list2 loop).

## 3. Additional Information From Student

Here is the merge method. The while loops and index variables seem to be correct.

![image](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/39ad6e85-9b7b-47e0-a950-d886f2c799ae)


## 4. Final TA Response
File & directory structure needed

![image](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/96b4b52d-2293-4e96-8193-bc1d4c48a69b)


Contents of each file before fixing the bug

![image](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/1f450e83-07ae-456a-8a80-acaa27a63c95)

![image](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/44dd759e-80db-4608-963a-a95a8d8d0105)

Full command line(s) ran to trigger the bug

**Description of what to edit to fix the bug

To fix this bug, you need to change the line containing the first if statement: if(list1.get(index1).compareTo(list2.get(index2)) > 0) to if(list1.get(index1).compareTo(list2.get(index2)) < 0) (the greater than operator is now a less than operator). This line compares the element at index1 in list1 to the element at index2 in list2. The bug made it so that if the first element was greater than the second element, then add the second element to the result list first, which made the list in descending order. By switching the sign, it will now merge in ascending order.

![image](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/3573579d-f904-48b1-9b29-ddf95768c085)

## 5. Reflection

Something new that I learned in CSE 15L was Vim. I have never used Vim before much less even heard of it. It is a very unique programming language and text editor, and I wouldn't say I loved it, but I did find it very interesting and useful for the last few labs. I am sure Vim will be useful in the future working with software, and I cannot wait to research it in further detail. 
