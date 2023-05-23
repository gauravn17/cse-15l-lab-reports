# Researching the `grep` Command:

**Command line options of 'grep' command I used on the files of directory 'technical' :** 

`grep -c` : Displays the number of lines that matches the given string/pattern in a file

This is useful when we want to count the number of times a particular string is repeated. For example, it may be particularly useful while working with massive files such as in a file with a DNA sequence, we can use this to find the number of adenine bases.

![Screenshot 2023-05-23 at 11 27 07 AM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/242cf72a-4911-4ec4-87d9-a3ddbfaeff77)


![Screenshot 2023-05-23 at 11 28 04 AM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/97132b25-d572-4da2-95b3-0bcd4d43ccb5)


`grep -w` : Checks for whole words in a file. Returns all the whole strings the given string is a part of in the file.

![Screenshot 2023-05-23 at 11 29 48 AM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/08f0265e-330c-48ec-bc63-99c99ab003bf)

![Screenshot 2023-05-23 at 11 30 04 AM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/984a48dd-3c91-4694-b0ca-51cbd680975b)


`grep -l` : Displays list of filenames that contain given pattern

![Screenshot 2023-05-23 at 11 31 35 AM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/61acd9bd-e268-4fe1-8cab-6851c536bff0)

![Screenshot 2023-05-23 at 11 31 56 AM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/f934300a-f5d3-48f5-a27b-20c032b3c6ec)

`grep -i` : Case insensitive search: searches for string/pattern case-insensitively

![Screenshot 2023-05-23 at 11 35 27 AM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/dba2f5c6-67bd-47b5-a1c2-63d18974258f)

![Screenshot 2023-05-23 at 11 35 09 AM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/e9e41759-aed6-4f4d-8110-a2c89094e86b)

Source I found all command options from : 

https://www.geeksforgeeks.org/grep-command-in-unixlinux/
