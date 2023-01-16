Lab Report 1 - VSCode installationa and Remotely connecting
=========
In the lab report, I will go through the process of installing Visual Studio Code, Connecting to remote server, and running some commands.

Part 1: Visual Studio Code
---------
Go to the Visual Studio Code website https://code.visualstudio.com/, follow the instructions to download and install it on your computer.
After installation, you should open Visual Studio Code and see the window as below: 
![Image](https://user-images.githubusercontent.com/97763875/211948568-b5439135-a12e-4b32-a585-6f5679438437.png)
Visual Studio Code is successfully installed and you are all set!

Part 2: Connect to remote server
---------
After you have installed Visual Studio Code, We will try to remotely connect to server. Make sure you have installed git if you are on Windows.

First, we should open the terminal on VSCode using Ctrl or Command + \`, or use the Terminal → New Terminal menu option. 
After setting up the password, we type `$ssh cs15lwi23zz@ieng6.ucsd.edu` to terminal with zz replaced by your course account.

It will prompt you to enter your password. When you have entered correctly, you will see the messages:
<img width="563" alt="Screen Shot 2023-01-16 at 2 12 57 PM" src="https://user-images.githubusercontent.com/97763875/212773182-7f9d41bc-a490-42d5-b086-a6dd1bcd38df.png">
This means you have successfully connected to remote server. 

Part 3: Trying some commands
---------
Now it's time to run some commands on your terminal.
`cd ~`
> To Home directory
'cd'
> To Home directory
`ls`
> To list files in current directory
`ls -a`
> To list all files including hidden files
`ls -lat`
> To list all files sorted by date
`pwd`
> Print current working directory
Here is a screenshot of possible outputs you can get:
<img width="835" alt="Screen Shot 2023-01-16 at 2 26 21 PM" src="https://user-images.githubusercontent.com/97763875/212774376-32ccc795-f0f9-41fe-8a5d-f4d1e2c19ba8.png">
Congratulations! Now you have learned how to instill Visual Studio Code, connecting to remote server, and run some commands. 
