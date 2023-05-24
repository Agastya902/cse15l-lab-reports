# **Lab Report - 3**
# **Researching Commands** 

## **Command Option 1: grep -c**
The ```grep -c``` command option shows the number of lines in which a specific word appears in a file. It is used with -r to allow us to search through the files in technical. In the image below, you can see that the command prints out the name of each file that it checked and the number of lines that contain the searched word.

Example 1: ```grep -c -r "world" technical```

![Image](grep -c.png)

In the above image, you can see that ```grep -c -r``` command goes through all th files in the directories of technical, and prints out the name of all the files along with the number of lines in which the searched string "world" appeared.

Example 2: ```grep -c -r "disaster" technical```

![Image](grep -c 2.png)

Here, we can see that the ```grep -c -r``` command searches through all the files in technical for the string "disaster". It returns 0 for most of the files as they do not contain that string in any of the lines. But, you can see that it has returned 5 for one of the file as "disaster" must have appeared in 5 lines in that file. 


