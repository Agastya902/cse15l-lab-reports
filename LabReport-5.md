# **Lab Report 5**

## **Part 1:** Debugging Scenario

### Student's Edstem post:
<img width="792" alt="Lab5 1 new" src="https://github.com/Agastya902/cse15l-lab-reports/assets/123341493/f8ad858f-28ab-40c1-84f6-37f00028c978">
<img width="791" alt="Lab5 2" src="https://github.com/Agastya902/cse15l-lab-reports/assets/123341493/93681071-92f7-40ff-acd0-dd579df6e7fc">

## **Response from TA:**
There is a small bug in your implementation of the AverageWithoutLowest method. Firstly, you need an instance variable that will identify the first appearance of the lowest element. We can achieve this by assigning a boolean variable ```start``` who's initial value is false. Secondly, there is an error in the return statement of the method. The length of the entire array is taken, whereas the occurence of the lowest element should be ignored while taking the length. That is, we should take ```arr.length - 1``` instead of ```arr.length```. The occurence of the lowest element is removed from the calculation by simply subtracting 1 from the length of the array.


## **Second Response from Student:**
Thank you so much! After changing the code using your guidelines, I was able to debug it sucessfully. I full understand why the code was buggy in the first place and also understood the part where we had to neglect the lowest element from the calculation. 
<img width="516" alt="Lab5 3" src="https://github.com/Agastya902/cse15l-lab-reports/assets/123341493/657eec90-c1e3-454c-ac9d-c50c1a1ded16">


## **Final response from TA:**
Here is a [link](https://github.com/ucsd-cse15l-w23/lab3) to the file structure required to sucessfully submit. This is the file before the bug fix: 
<img width="746" alt="Lab5 5" src="https://github.com/Agastya902/cse15l-lab-reports/assets/123341493/4d76b650-51b1-48a8-8427-d8bf56cc6158">


## **Part 2:** Reflection
I found the part about Vim commands really interesting. The grep commands gave me an insight. I also learnt how to navigate in the terminal using the keyboard. The setting up of an ssh key in the lab was also a very convenient way to log in. 
