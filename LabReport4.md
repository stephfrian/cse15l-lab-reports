# Lab Report 4: Competition Tasks
By Stephanie Frianeza

Competition Instructions:
1. Delete any existing forks of the repository you have on your account
2. Setup Fork the repository
3. The real deal Start the timer!
4. Log into ieng6
5. Clone your fork of the repository from your Github account
6. Run the tests, demonstrating that they fail
7. Edit the code file to fix the failing test
8. Run the tests, demonstrating that they now succeed
9. Commit and push the resulting change to your Github account (you can pick any commit message!)

## Step 4: Logging Into ieng6
![pasted image 0](https://user-images.githubusercontent.com/110694499/221438108-5bf3c1fa-f031-4677-9d94-f80f8f70d0df.png)

Keys pressed: `<up><enter>`

The 'ssh cs15lwi23agp@ieng6.ucsd.edu' was one up in the search history so I used the up arrow once to access it, then pressed enter to log in. I didn't have to type in my password because I generated SSH Keys for ieng6.

## Step 5: Cloning Fork of the Repository From GitHub
![pasted image 0 (1)](https://user-images.githubusercontent.com/110694499/221438126-6b271d7f-88d3-403d-a254-16f878c29071.png)

Keys pressed/Typed: Typed `git clone git@github.com:stephfrian/lab7.git`, `<enter>`, `cd la<tab>`

I didn't have the git clone command saved in my history, so I manually typed out the aforementioned command, copying and pasting the .git file from GitHub forked repository. I then cd'ed into the lab 7 directory using the <tab> key to autofill the name of the directory.

## Step 6: Running the Tests, Demonstrating They Fail
![pasted image 0 (2)](https://user-images.githubusercontent.com/110694499/221438207-f68b4bf9-df62-4bcc-97c6-98402a12a1c6.png)
  
Keys pressed/Typed: `javac Te<tab>` `<enter>`

I typed `javac Te<tab>` because I didn't have the javac command saved in my search history. I used the tab key after typing "Te" to autofill the TestListExamples.java file. Then I pressed "enter" to run the tests and demonstrate they fail.
  
## Step 7: Editing the Code File to Fix the Failing Test
![pasted image 0 (3)](https://user-images.githubusercontent.com/110694499/221438289-d3db8456-9473-48a2-893d-2cc62296a108.png)
![pasted image 0 (4)](https://user-images.githubusercontent.com/110694499/221438294-5f0d0c8f-42b5-405e-bef1-8fa66192655e.png)
  
 Keys pressed: `nano Li<tab>.java`, `<down>` 42 times, `<right>` 12 times, `<backspace>`, Type `2`, `<Ctrl><O>`, `<enter>`, `<Ctrl><X>`
  
 After using the nano command, I made one edit to the .java file: changing index1 += 1 to index2 += 1. Then I saved this edit to the file and exited the nano window
  
 ## Step 8: Running the Tests, Demonstrating That They Succeed
  ![Screenshot 2023-02-27 181718](https://user-images.githubusercontent.com/110694499/221736137-7686e7e3-64aa-4b88-9715-04a25402dc5d.jpg)
 

Keys pressed: `<Ctrl><R>`,`javac - <enter>`, `<Ctrl><R>`, `java - <enter>`

 I used the reverse-i-search command <Ctrl><R> to search through my command history for the javac command that compiles my tester file. Then I used the same command to search for the javac command that runs my tester file. 
  
  ## Step 9: Committing and Pushing the Resulting Change to My Github Account 
