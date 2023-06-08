# **Lab report 4**
**In this Lab report I will show the steps on how to complete the following tasks:** 
Step 1: Log into ieng6

Step 2: Clone your fork of the repository from your Github account

Step 3: Run the tests, demonstrating that they fail

Step 4: Edit the code file to fix the failing test

Step 5: Run the tests, demonstrating that they now succeed

Step 6: Commit and push the resulting change to your Github account

## **Step 1** Logging into ```ieng6```
First I typed in the following command: ```ssh cs15lsp23gv@ieng6.ucsd.edu```. Here, ```gv``` is my account specific code. I then pressed <Enter>.
  
<img width="569" alt="Screenshot 2023-06-07 at 7 25 33 PM" src="https://github.com/Agastya902/cse15l-lab-reports/assets/123341493/c0aa420b-393a-4090-b8bb-ccad423ab790">

## **Step 2:** Clone your fork of the repository from your Github account
First, I typed the command ```git clone git@github.com:ucsd-cse15l-sp23/lab7.git``` and then i pressed <Enter>. This command downloads all the files from the repository.
  
<img width="594" alt="Screenshot 2023-06-07 at 7 36 32 PM" src="https://github.com/Agastya902/cse15l-lab-reports/assets/123341493/703af0e3-bca5-4c1c-9feb-c1fa375e1904">

## **Step 3:** Run the tests, demonstrating that they fail
First, I changed the working directory to lab7. I executed this command: ```cd lab7```. Then, ```ls``` shows the contents of the directory. Now, I pressed <Ctrl + R> and typed <javac> and looked for ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java``` command. Then <Enter> and then pressed <Ctrl + R> and java -> to look for ```java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.jUnitCore ListExamplesTests ``` and then pressed <Enter>. The <Ctrl + R> is used to search through history and javac is used to compile all the files in the current directory. As shown in the screenshot below.
  
<img width="963" alt="Screenshot 2023-06-07 at 7 40 07 PM" src="https://github.com/Agastya902/cse15l-lab-reports/assets/123341493/18776c5c-a44e-485c-825d-e0daeba9cde1">


## **Step 4:** Edit the code file to fix the failing test
I typed ```nano Li``` and <Tab> to complete it to nano ListExamples and typed <.j> and <Tab> to complete it to ```nano ListExamples.java``` then <Enter>. Then, I clicked <down> 14 times and <right> 22 times followed by <backspace> 3 times to fix one of the bugs. To fix the second bug, I pressed <down> 28 times and <left> 5 times followed by <backspace> to fix it. Now to save the changes: I pressed <Ctrl + 0> and <Enter>. To exit nano I pressed <Ctrl + X>.
  
<img width="1119" alt="Screenshot 2023-06-07 at 7 41 53 PM" src="https://github.com/Agastya902/cse15l-lab-reports/assets/123341493/f420397e-e49f-4552-9e66-6a0e7026b893">

## **Step 5:** Run the tests, demonstrating that they now succeed
To get back to ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java``` I pressed <up> 4 times. Then ````javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamples````  <Enter> to run all the tests again 

## **Step 6:** Commit and push the resulting change to your Github account
I then clicked git add . command to prepare the changes. Then, ```git commit -m "Fixed"``` to commit changes with the message "Fixed". Then i typed ```git push``` command to push all the changes to git hub.
