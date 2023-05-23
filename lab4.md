# Lab Report 4

# Step 1: Log into ieng6

For Step 1, I logged into ieng6 with by ssh-ing into my account, using ssh cs15lsp23es@ieng6.ucsd.edu and my password.

# Step 2: Clone your fork of the repository from your GitHub account

For Step 2, I copied the HTTPS URL of the lab7 fork from my GitHub account, typed git clone https://github.com/gauravn17/lab7.git), which cloned the repository into my ssh account.

# Step 3: Run the tests, demonstrating that they fail

For this step, I changed to the lab7 directory by typing cd l, pressing <tab> to autocomplete it, and pressing <enter>. I then typed ls and <enter> to list all the files/directories in lab7. Finally, I typed bash t, <tab> to autocomplete to bash test.sh, and pressed <enter>, which ran the tests (and showed that they failed).

# Step 4: Edit the code file to fix the failing test
For this step, I typed vim L and <tab> to autocomplete to vim ListExamples, then typed .java at the end, and finally pressed <enter>. This opens Vim and the file that needs to be edited in the terminal.

Next, the cursor was already on top of the 1 that I needed to change in ListExamples, so I simply typed x to delete the 1. This was done in Vim's normal mode.

I then pressed i to enter insert mode in Vim, and typed 2 to correct the error.

Finally, I pressed the <esc> key to switch back to normal mode in Vim, and then typed :wq to exit Vim and save the file.

# Step 5: Run the tests, demonstrating that they now succeed
For this step, I re-ran the tests by pressing <up><up> and then <enter> to run bash test.sh again, this time showing that the tests passed.


# Step 6: Commit and push the resulting change to your Github account
For this final step, I typed git add L then pressed <tab> to autocomplete to git add ListExamples, then typed .java at the end and pressed <enter>. This git action tracks the file so that when git commit is called, it knows which one(s) to include. I then typed git commit -m "changes" and pressed <enter>. This git action records the repository changes. Finally, I typed git push and <enter>, my username keeanalbao and <enter>, and my GitHub password and <enter>. This does the action of updating the commit changes and sending it to the remote repository.
