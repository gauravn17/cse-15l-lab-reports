# Lab Report 5

## 1. EdStem Post from Student : EDSTEM thread 05/06/23

## **What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?**

Visual Studio Code & JUnit

## **Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.**

I am trying to debug the Sort.java file to sort two arrays in ascending order using selection sort, and both the `testSelection1` and `testSelection2` tests are failing . Here are the screenshots of the  `Sort.java` and `SelectionSortTests.java` files , as well as my `bash` script, `test.sh`  :

![Screenshot 2023-06-05 at 10 57 45 PM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/ef40ceae-0a67-4127-a667-2d9f6891654c)

![Screenshot 2023-06-05 at 10 42 40 PM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/081db1b0-9ea8-4a45-a12e-a51fdd67c45f)


![Screenshot 2023-06-05 at 10 42 43 PM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/4e585194-03a3-4465-afd3-0909f70c144e)

The lists are supposed to be merged in ascending order, but instead, they appear to be getting merged in descending order.

## **Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.**

 Below is the command I'm running `bash test.sh`, with its output, which is both JUnit test runs failing.
 
![Screenshot 2023-06-05 at 10 35 29 PM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/90563b4c-22bb-4b62-ae78-de5fbba3af29)


## 2. TA Response 1 :

Can I see the code for your selection sort method so I can look through the logic of the method and we can debug from there?

## 3. Response from Student

Here is the `selection sort` method. I am pretty sure the  `while` loops and `if` statements are correct, and am unsure why my tests are failing.

![Screenshot 2023-06-05 at 10 42 36 PM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/dbf65967-2c55-471b-b8e2-9ce1db1d89ac)

## 4. Final TA Response

Let us look at the file & directory structure.
 
![Screenshot 2023-06-05 at 11 00 41 PM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/85dafe52-d449-4924-9747-63af64c9a203)

**Description of solution**

To fix this bug, you must change the line containing the first `if` statement: `if(arr[j] > arr[index])` to `if(arr[j] < arr[index])` (replace the greater than operator with a less than operator). This bug was causing the greater of the two elements compared at each iteration to be assigned to arr , instead of the lesser of the two elements. Thus, the bug was causing the array to be sorted in descending order instead of ascending order. By switching the sign from `>` to `<`, the bug is fixed, and the code will now sort the lists in ascending order.

Updated code:

![Screenshot 2023-06-05 at 10 57 52 PM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/5155ddde-b188-46ba-bd82-d15fa30f704c)


## 5. Reflection

Something new that I learned in CSE 15L was Vim. I had never used Vim before, and found it very interesting how it could be used to edit files from the command line itself,and I am sure Vim will be a powerful tool in the future working with software. I cannot wait to research it in further detail. I also gained a better understanding of working with files and navigating directories (with commands such as `cd`,`ls` ,`pwd`, etc) which is something that is invaluable in troubleshooting even in my programming assignments for other classes.
