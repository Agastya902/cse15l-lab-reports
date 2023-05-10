# **Lab Report 2 - Server and Bugs (Week 3)**

## **Part 1:** ``String Server``

This part of the lab report required me to create a new server called ``StringServer``. When the path of the URL is changed, a string is displayed on the web page. If we further change the path of the URL, a new string is displayed in the next line along with the previous string. The image attached below shows my code for the ```StringServer``` class. These classes are similar to the files that we worked with in Lab while creating ```NumberServer```.

```
import java.io.IOException;
import java.net.URI;

class StringHandler implements URLHandler 
{

    int num = 0;
    String newString = "";

    public String handleRequest(URI url) 
    {
        if (url.getPath().equals("/")) 
        {
            return "";
        }
        else 
        {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add-message")) 
            {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) 
                {
                    newString += parameters[1] +"\n";
                     
                }
                return newString;
            }
            return "404 Not Found!";
        }
    }
}

class StringServer 
{
    public static void main(String[] args) throws IOException 
    {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new StringHandler());
    }
}
```


### **Implementation of /add-message**

1. **/add-message?s=hi**
   When the above path is typed after localhost:4003, the ``StringHandler`` method is called which further calls the handle method. The handle method is called with the URI as the argument. In the ``StringHandler`` class, the program checks if the path has ``/add-message`` in it. When ``/add-message`` is found, the program creates an array which holds the contents of the String after the "=" sign. 
   
![Image](labss1.png)

2. **/add-message?s=ronnie**
   When the above path is typed in after the previous attempt, the handle method in ``StringHandler`` with the URI is called again. Now the program checks if the ``/add-message`` exists in the path. Then it creates an array which stores the string after the "=" sign. Here it is "ronnie". Now the given string ("ronnie") is printed in a new line because we used "/n" in the previous iteration.
   
![Image](labss2.png)   

## **Part 2:**
I chose the bug in the ```reverseInPlace``` method of the ```ArrayExamples``` class.

**Input that induces failure**
```@Test
  public void testReverseInPlace1() 
  {
    int[] input1 = {0, 1, 2, 3, 4, 5};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{5, 4, 3, 2, 1, 0}, input1);
  }
  ```
  **Input that does not induce a failure**
  ```@Test 
	public void testReverseInPlace() 
  {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
```

### **Symptom:**

![Image](labss3.png)

**Code before Bug fix:**
```
static void reverseInPlace(int[] arr) 
  {
    for(int i = 0; i < arr.length; i += 1) 
    {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
The Bug in this code is that it does not actually reverse the array. Instead, it overwrites each element of the array with the corresponding element from the end of the array. This means that when the iteration gets to the halfway point, it overwrites elements that have already been changed. As a result, the final array ends up being the same as the original.

To Debug this code, we need to swap the elements, without overwriting, at opposite ends of the array.

**Code after the Bug fix:**
```
static void reverseInPlace(int[] arr) 
{
  for(int i = 0; i < arr.length/2; i++) 
  {
    int temp = arr[i];
    arr[i] = arr[arr.length - i - 1];
    arr[arr.length - i - 1] = temp;
  }
}
```

**Explanation of the Bug fix:**

The codeblock above shows the correct version of the Buggy code. In the Debugged version, we use a loop that goes halfway through the array up to the mid point. For each iteration, we swap the element at i with the element at the corresponding position from the end of the array ```(arr.length - i - 1)```. This way we have ensured that each element is swapped only once and the array is correctly reversed. This swapping was done in order to insure that the elements are swapped instead of overwritten. 

## **Part 3:**

Lab in Week 2 introduced us to the inner workings of a web page. I think that this was really helpful because we use we pages for even simple things now days. After running the server on a remote computer in the CSE basement, I got a URL that could be accessed from any device. The most exciting part was that when editing the server, the change was displayed immediately on the web page that i created.
Lab in Week 3 was about Server and bugs. We were taught the basics of testing a code using jUnit testing. We were also given a thoughtful insigt on how we can use symptoms and testing to find bugs and fix the code. I think that this will also help me in CSE12 which I am taking this quarter.


   
   
