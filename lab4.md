# Lab Report 4

# Step 1: Log into ieng6

For Step 1, I logged into ieng6 with by ssh-ing into my account, using ssh cs15lsp23es@ieng6.ucsd.edu and my password.

![Screenshot 2023-05-22 at 8 38 20 PM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/edc85a15-d5d4-4e02-abfc-5d0a74010126)

# Step 2: Clone your fork of the repository from your GitHub account

For Step 2, I copied the HTTPS URL of the lab7 fork from my GitHub account, typed git clone <Ctrl V <HTTPS URL of lab 7 fork> > , which cloned the repository into my ssh account.

![Screenshot 2023-05-22 at 8 40 50 PM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/b35e0ef0-42ac-47fe-8476-02477a8d2977)

![Screenshot 2023-05-22 at 8 43 46 PM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/0b205e6a-b8ca-4bf7-a0e3-4f71f5dd6cd9)


# Step 3: Run the tests, demonstrating that they fail

For Step 3 , I navigated into the 'lab7' directory by typing cd lab7. I then typed ls  to view all the file names contained in lab7. Finally, I typed bash test.sh, which ran the tests , while showing that they failed.
  
 ![Screenshot 2023-05-22 at 8 49 36 PM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/25360ce3-2231-43ac-b2cd-a4767d2bf0ac)


# Step 4: Edit the code file to fix the failing test
For Step 4, I typed vim ListExamples.java, which opened Vim and the file, 'ListExamples.java' that needs to be edited in the terminal.
  

Next, the cursor was already on top of the 1 that I needed to change in ListExamples, so I typed x to delete the 1. This was done in Vim's normal mode.

I then pressed i to enter insert mode in Vim, and typed 2 to correct the error
  
  ![Screenshot 2023-05-22 at 9 04 02 PM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/17ef8b81-69c5-4f23-bab8-06a47e388263)


Finally, I pressed the <esc> to switch back to normal mode in Vim, and then typed ```:wq``` to exit Vim and save the file.
  
![Screenshot 2023-05-22 at 9 05 33 PM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/99ceb63c-0f48-44ec-8351-976597309562)

# Step 5: Run the tests, demonstrating that they now succeed

  For this step, I re-ran the tests by doing bash test.sh again, this time showing that the tests passed.

  ![Screenshot 2023-05-22 at 9 09 29 PM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/f13f7917-f13e-4819-a365-670517f6c2a7)


# Step 6: Commit and push the resulting change to your Github account
  
 For this step, I used git add ListExamples.java to track the file so that when git commit is called, it knows which file to include. I then typed git commit -m "changes" to record the repository changes. Finally, I typed git push, my username gauravn17 , and my GitHub password . This updated the commit changes and sent them to the remote repository.
  
 ![Screenshot 2023-05-22 at 9 36 27 PM](https://github.com/gauravn17/cse-15l-lab-reports/assets/93863977/d8274215-3369-46d6-83a8-1eff93f328a0)

 

  
