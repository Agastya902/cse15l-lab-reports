# **Lab Report 1 - Remote Access and FileSystem (Week 1)**

**Step 1:** Installing VS code

Go to the Visual Studio Code website [https://code.visualstudio.com/](https://code.visualstudio.com/), and follow the steps to download. There are multiple versions of VS code depending upon the operating system being used. Click on the correct version of VScode that you want to install (Mac or Windows). Wait untill the download finishes and then open VS code. The image below shows what VS code should look like after successful installation (it might have different colors depending upon the operating system).

![Image](Screenshot 2023-04-10 at 4.11.30 PM.png)

**Step 2:** Remotely Connecting

Open Terminal and type in the following command: ```ssh cs15lsp23gv@ieng6.ucsd.edu```. A prompt will come up allowing you to enter your account password. Now type in your password (there is no indication while typing) and it should work. If done correctly, it should show ```Prepping cse15lsp23```. Now your terminal is connected to a computer in the CSE Basement and any commands that you run will run on that computer. 

![Image](Screenshot 2023-04-06 at 11.03.14 AM.png)

**Step 3:** Trying some Commands

Now test some commands like ```cd, ls, pwd, mkdir``` by typing them directly. After running these commands, the desired output will be attained if the connection was successful. After trying to change the directory using the cd command, no visible output was attained in the terminal. After running the pwd command, it gave us the present working directory (```/home/linux/ieng6/cse15lsp23/cse15lsp23gv```). The list command (ls) only listed the directory "perl5" as the output.

![Image](Screenshot 2023-04-06 at 11.19.57 AM.png)
