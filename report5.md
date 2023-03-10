# Lab Report 5

The lab report that I enjoyed the most was the Week 7 Lab: CLDQ - CSE Labs "Done Quick". I enjoyed it because I was able to get one of the fastest times in the class. Additionally, it was fun competing with the other students.

### How I did the task

After the basic setup steps to do the task, I was able to complete the task very fast by storing the URL of the GitHub repository in my clipboard. After that, I was able to run the commands to run the tests on the code by storing them in my terminal history. After that, I edited the code file quickly by spamming my down arrow key, and using the keyboard shortcuts to save my changes to the file. I ran the tests again through the saved commands in my terminal history. Finally, I was able to quickly commit and push my changes to GitHub by typing fast.

### Doing the task differently

The task could've been completed very quickly if I used a bash script. A bash script is just a file that contains a bunch of terminal commands. I could've put all of the commands within the bash script file, and ran the file, which would've instantaneously ran all the necessary commands. This would've allowed me to do the task so much faster. 

If I had to complete the task now using bash scripts, I would have two bash scripts, one for all the commands before editing the file, and one for all the commands after editing the file. This is because, I would still have to manually edit the file and save the changes. 

The first bash script would contain the following code:

```
set -e
ssh cs15lwi23afk@ieng6.ucsd.edu
git clone git@github.com:anishkasam/lab7.git
cd lab7
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
nano ListExamples.java
```

These commands would ssh into my ieng6 account, clone my fork of the lab7 repository, cd into it, run the JUnit tests, and finally open the nano editor. From here, I would manually go down to the line with the error and fix it, save my changes, and then close the file. Then I would run the second bash script.

The second bash script would contain the following code:

```
set -e
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
git add .
git commit -m "fix error"
git push
```

These commands would rerun the JUnit tests on the updated file, add my changes to a commit, add a commit message, and then push the commit to GitHub. Storing all of these commands in a bash script could've made my time for this lab much much faster.
