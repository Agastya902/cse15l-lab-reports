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

## **Command Option 2: grep -r**
The ```grep -r``` command searches the directory and subdirectories for a specific string. Then, it prints out the path to the given file and the line in which the string appears.

Example 1: ```grep -r "escape" technical```

![Image](grep -r.png)

In the image above, the ```grep -r``` command searches the directories and subdirectories of technical. As a result, it prints out the names of the files and the lines in which the specified string "escape" appears. We can see that the searched string is highlighted in red in the terminal.

Example 2: ```grep -r "saved" technical```

![Image](grep -r 2.png)

In Example 2, we can see that ```grep -r``` searches technical for the string "saved". As a result, it returns the name of the file and also the lines which contain the specified string.


