# CSE 15L Lab Report-3-week6

## Ziyu Wang ziw003@ucsd.edu

### Choice 3: Copy whole directories with scp -r

#### 1. Copy whole markdown-parse directory to ieng6 account.

![Image](https://user-images.githubusercontent.com/57332517/153525408-be201f3d-cd8b-43d3-bbab-31c2bd06ba79.png)

#### 2. In the account, compile and run the tests.

![Image](https://user-images.githubusercontent.com/57332517/153525506-a309d0a8-48b4-4f6a-b42f-7f3bae66a30e.png)


#### 3. Copy whole directory and run test in one line command.  **Error here**

       a. Remove the original directory first.
  
  ![Image](https://user-images.githubusercontent.com/57332517/153525907-af40ccd6-9696-4940-a3b1-a635dda64028.png)
        
       
       b. One-line command.
 
I went to office hours, tutor Justin and I both think my one-line command is correct, and I did the same command separetely on the server to run the test. Here is the output.

![Image](https://user-images.githubusercontent.com/57332517/153526899-46b17657-8e67-43b9-947f-8e38f1577b25.png)

![Image](https://user-images.githubusercontent.com/57332517/153526967-1a6e10b7-8250-4b75-98c1-2f93239b3e2c.png)

The following is my thoughts and discussion with tutor:

1. I can run tests separately on my server after the scp -r, so the copy is correct.
2. I try "ls" or "cd" together after ssh, it is correct, so the grammar and syntax is correct.
3. I try ```java -version``` separately on server and in one-line command after ssh, it provides different output, which is weird. On server, I have normal java, but in one-line,
it is about the jdk version, which is weird.
4. The error about cannot find symbol for ```Path.of``` and ```Files.readString``` is the same one I had in the very beginning of this quarter, which is fixed by updating my locol computer's java to latest version. For this problem, it's because the old version of java has different method and name for Path and Files class, so I am not sure whether it's the same issue on the server. 
5. From the discussion with tutor, I tried serveral methods, including the ```*```, the ```&&```, and the ```javac MarkdownParse.java``` first. They basically have the same cannot find symbol.
6. The line is written on Thursday 6:20 p.m. 2/10/2022, if no solution is found until Friday 2/11/2022, this line will remain unchanged. Sorry for the error.




**Thank you for reading.**
