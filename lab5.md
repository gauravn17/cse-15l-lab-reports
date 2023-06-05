# Lab Report 5

## 1. Student EdStem Question

**What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?**

Visual Studio Code & JUnit

**Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.**

I am trying to debug the ListExamples.java file, and both the testMerge1 and testMerge2 tests are failing . Here are the screenshots of the  tests running (symptom):

![image](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/769d3a33-a212-4b7b-8162-deeeee34f46d)

![image](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/43725159-ffb8-4d01-ad9f-2a4d1a9b3131)

The lists are supposed to be merged in ascending order, but instead, they seem to be getting merged in descending order.

**Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.**

 Below is the command I'm running.
 
 ![Screenshot 2023-06-05 at 2 59 34 PM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/d20e6da7-b996-4a4b-bffb-7ab1a501753c)

## 2. Initial TA Response

Can I see the code for your merge method so I can look through the logic of the method and we can debug from there?

## 3. Additional Information From Student

Here is the merge method. I am pretty sure the  `while` loops , `if` statements and index variables are correct.

![image](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/39ad6e85-9b7b-47e0-a950-d886f2c799ae)

## 4. Final TA Response

Let us look at the file & directory structure.

![image](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/96b4b52d-2293-4e96-8193-bc1d4c48a69b)


Let us look through the contents of each file before fixing the bug

![image](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/1f450e83-07ae-456a-8a80-acaa27a63c95)

![image](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/44dd759e-80db-4608-963a-a95a8d8d0105)


**Description of edits to fix the bug**

To fix this bug, you must change the line containing the first `if` statement: `if(list1.get(index1).compareTo(list2.get(index2)) > 0)` to `if(list1.get(index1).compareTo(list2.get(index2)) < 0)` (replace the greater than operator with a less than operator). This line compares the element at `index1`in `list1` to the element at `index2` in `list2`. This bug was causing greater of the two elements compared at each iteration to be added to the results list, instead of the lesser of the two elements. Thus, the bug was causing the list to be merged in descending order instead of ascending order. By switching the sign from `>` to `<`, the bug is fixed, and the code will now merge the lists in ascending order.

![image](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/3573579d-f904-48b1-9b29-ddf95768c085)

## 5. Reflection

Something new that I learned in CSE 15L was Vim. I had never used Vim before, and found it very interesting how it could be used to edit files from the command line itself,and I am sure Vim will be a powerful tool in the future working with software. I cannot wait to research it in further detail. I also gained a better understanding of working with files and navigating directories, something that is invaluable in troubleshooting even in my programming assignments for other classes.
