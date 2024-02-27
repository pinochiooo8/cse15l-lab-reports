# Lab Report 4

## 1. Setup Delete any existing forks of the repository you have on your account

## 2. Setup Fork the repository

## 3. The real deal Start the timer!

## 4. Log into ieng6
  Enter the ssh rucao@ieng6.ucsd.edu in the terminal to log into ieng6 and press <enter>
  ![Image](step4.png)

## 5. Clone your fork of the repository from your GitHub account (using the SSH URL)
  Copy and paste the SSH URL from my GitHub account. 
  ![Image](step5.png)
  
## 6. Run the tests, demonstrating that they fail
  Type in <ls><enter> to see the list of files under the repository, and type <cat test.sh> to view the content file. <command+C> to copy the javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java command, 
  <command+v> to paste command and hit <enter>. <command+C> to copy thejava -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ... command and  <command+v> to paste the command and hit <enter>. 
  ![Image](step6.png)

## 7. Edit the code file to fix the failing test
  Type in vim ListExample.java to edit the file. 
  Press <SHIFT + G> to Move me to the bottom of the file, Press<k><k><k><k><k><k> move me to the line that needs to be edited, <control + A> gets me to the start of the line, press <dw> to delete the integer 1, press <i> <2> <space>to 
  add an integer 2 and hit <esc> to quit the insert mode. press <:wq> to save and exit vim. 
  ![Image](step7.png)

## 8. Run the tests, demonstrating that they now succeed
  Keys pressed: <up><up><up><enter>, <up><up><enter> The javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java command was 3 up in the search history, so I used up arrow to access it. 
  Then the java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ... command was 2 up in the history, so I accessed and ran it in the same way.
  ![Image](step8.png)

## 9. Commit and push the resulting change to your GitHub account (you can pick any commit message!)
  Use git commit and git add to push the resulting change to the remote repository. 
  ![Image](step9.png)
  ![Image](step9-1.png)
## Summary 

 ### Commands: 
   1. git clone: Clone my fork of the repository from my GitHub account.
   2. ls: show the list of files under the current directory.
   3. vim: to open the vim editor.
   4. cat: show the content of the input file.
   5. javac, java: compile and run the java file.
   6. git commit: records changes to the repository, capturing the current state of the tracked files.
   7. git add: stages changes in files to be included in the next commit, allowing you to select specific modifications to commit.
   8. git push: push my commits to the remote repository associated with my current branch.
      
 ### Keypresses:
   1. <command+C>,<command+v> : copy and paste.
   2. <SHIFT + G>: Under Vim, Move to the bottom of the file.
   3. <control + A>: Under Vim, Move to the start of the line
   4. <dw> : under vim, delete.
   5. <i> : under vim, insert.
   6. <:wq>: under vim, save and exit vim.
   7. <esc>: under vim, in this particular lab the function is to exit the insert mode. 
