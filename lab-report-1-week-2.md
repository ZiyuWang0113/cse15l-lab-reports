# CSE 15L Lab Report-1-week2

## Ziyu Wang ziw003@ucsd.edu
-----
### VScode
Go to [Link](https://code.visualstudio.com/) and download the correct version for your operating system. The VSCode should be like this.
* Add junit to path: press `Ctrl + Shift + P`, enter `java : config` choose classpath, add the source library with your jar file.
* Change color theme: press `Ctrl + Shift + P`, enter `theme`, search and select your preferred themes.

<img src="https://user-images.githubusercontent.com/57332517/149253827-9929a540-a25c-4b22-806b-e24279a0f494.png" width="400" height="324">

### Course account on `ieng6`
To connect to CSE 15L course account, follow these steps:

1. Find your account name on [Link](https://sdacs.ucsd.edu/~icc/index.php)
2. Install and Open Vscode, go to `Terminal`, enter `ssh cs15lwi22***@ieng6.ucsd.edu` where *** represents your own ID.
3. Enter password, and the terminal will like this.
4. You will need to reset password if your old one doesn't work.
<img src="https://user-images.githubusercontent.com/57332517/149253376-b4cba662-0d67-467a-b678-fe5d02c1975d.png" width="324" height="324">

### Commands
Try some commands like `cd`, `ls`, `pwd`, `mkdir` in the terminal.

`cd` means change directory, you should enter your expected directory after `cd` such as ```cd desktop/cse15l```.

`ls` means list, it will list all files under current directory. However, it hides some files whose name starts with `.`, so use `ls -a` to display all files.

![Image](https://user-images.githubusercontent.com/57332517/149254621-995667fb-995f-4822-87a5-a2ecaf8b8e46.png)

`pwd` shows the complete path for current directory.

![图片](https://user-images.githubusercontent.com/57332517/149254753-fc655500-d905-45f8-94a4-467f041e8f5b.png)

`mkdir` will create a new directory ofyour given name.

### Move files with scp

Using `scp WhereAmI.java cs15lwi22***@ieng6.ucsd.edu:~/` We can have the file moving to the server online.

![Image](https://user-images.githubusercontent.com/57332517/149255627-e7da6c7f-d23d-42a7-8ecc-3095f76aba7b.png)

### Set an SSH key
I use Windows, so I follow the extra steps:

1. Run the code `ssh-keygen -t ed25519` on terminal. It will display like 

```Generating public/private ed25519 key pair. Enter file in which to save the key (C:\Users\username\.ssh\id_ed25519):```

2. Press `Enter` for default file, and yor will receive the strange SSH key, such as:

![Image](https://user-images.githubusercontent.com/57332517/149256053-0164d7ef-a42e-46cf-b719-19589446150d.png)

3. You will see two new files on your system; the private key (in a file id_rsa) and the public key (in a file id_rsa.pub), stored in the .ssh directory on your computer.

4. Copy the public key to `.ssh` directory of your server account, use `ssh` again, enter password, enter `mkdir .ssh`, `logout`, `scp /Users/***/.ssh/id_rsa.pub cs15lwi***@ieng6.ucsd.edu:~/.ssh/authorized_keys` which `***` is your user name.

Now you can skip the password when doing commands.

### Optimize running
You can write a command in quotes after of an ssh command to directly run it on the server, then exit. For exmaple,

`ssh cs15lwi22***@ieng6.ucsd.edu "ls"` or `ssh cs15lwi22***@ieng6.ucsd.edu "cd cse15l"`

You can also use semicolons to run multiple commands, like

`cp WhereAmI.java cse12.java; javac cse12.java; java WhereAmI`

You can also run both the compile `javac` and run `java` command both on the server like:

`ssh cs15lwi22@ieng6.ucsd.edu "javac Config.java; java Config"`. For example, compile and run WhereAmI.java:

![Image](https://user-images.githubusercontent.com/57332517/149257249-9ddcd679-8863-4f91-842c-f88ce463400a.png)

### More about GitHub
Not required on this report? 
But this links refers to my `index.md` in github: https://github.com/ZiyuWang0113/cse15l-lab-reports/blob/main/index.md.

And this links goes to my cse15l-lab on github: https://github.com/ZiyuWang0113/cse15l-lab-reports.

#### Thank you for reading. #### 
