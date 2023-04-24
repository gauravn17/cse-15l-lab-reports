# **Tutorial for CSE 15L students to log into a course-specific account on ieng6**:
    
* Look up your course-specific account for CSE15L here and reset your password:

   [Link](https://sdacs.ucsd.edu/~icc/index.php)

 **Installing VS code**:
  
 * Download VS code from the link below
 
   [Link](https://code.visualstudio.com/download)
  
  Once intalled, open VS code. It should look like this:
  
  ![Image](VSCODE.png)
  
  __Remotely Connecting__:
  
  * To remotely connect into a course-specific account on ieng6, create a new file on VS CODE and click 'New Terminal' from the 'Terminal' option at the top of the screen. Once a new terminal has opened, type 'ssh ' followed by your course-specific id , followed by '@ieng6.ucsd.edu'.
  For example, the remote login for id cse15lsp23zz will be 'ssh cse15lsp23z@ieng6.ucsd.edu'.
  
  Once logged in remotely, the terminal should look like this:
  
  ![Image](RemoteLogin.png)
  
  __Running commands__:
  
  Try running the commands cd, ls, pwd, mkdir, and cp a few times in different ways, both on your computer, and on the remote computer after ssh-ing (use the terminal in VScode).
  
  ![Image](Commands.png)
  
 The command I used in the image above is ps ax. This command displays an overview of all processes that are running, which is helpful to understand and troubleshoot the system.
 
 Other useful, basic commands are:

 * _ssh_: Perhaps the most important command, ssh stands for 'Secure shell'. It is used to log into a computer over an unsecured network, as used in the 'Remotely Connecting' step of this tutorial.
 *  *cd* : Stands for 'change directory', used to change the current directory of the terminal. 
 *  _ls_ : Stands for 'list', used to list the names and features of files and directories.
 *  _pwd_: Prints the full name or path of the current dictory.
 
  
