# CSE 15L Lab Report-4-week8

## Ziyu Wang ziw003@ucsd.edu

Link to my repository: [My](https://github.com/ZiyuWang0113/markdown-parse-new)

Link to reviewed repository: [Reviewed](https://github.com/kathyychenn/markdown-parse)

### Snippet 1

Should be: 

![图片](https://user-images.githubusercontent.com/57332517/155637710-5cc31f6c-de1c-42fa-a4a1-7efa370f38b6.png)

Test in VScode:

![图片](https://user-images.githubusercontent.com/57332517/155638527-68627d84-de88-4e6f-8bb9-90f4aabae245.png)

For my implementation:

![图片](https://user-images.githubusercontent.com/57332517/155639450-a77040d5-d50a-492e-b9b9-6ff6584d4ca5.png)

For reviewed implementation:

![图片](https://user-images.githubusercontent.com/57332517/155638678-0c8d9027-226b-41a2-8d9a-3663aac2161c.png)

Both of the implementations have same wrong output.
I think there can be a small code change to fix it. It should check the \` between bracket so when there are two of them, the characters turn into a code block. So, maybe create a new varibale to trace the location for \`, and then check whether the brackets still work. In the parentheses， the \` can be igored since the parentheses has higher priority so the link will be kept. I would say 10 line is roughly enough.


### Snippet 2

Should be: 

![图片](https://user-images.githubusercontent.com/57332517/155639742-7ae00327-5ac3-45b9-8200-c4b499c36446.png)

Test in VScode:

![图片](https://user-images.githubusercontent.com/57332517/155641473-75a28e03-6783-416e-99f0-6cc1851e6e88.png)

For my implementation:

![图片](https://user-images.githubusercontent.com/57332517/155641699-59729029-f57c-4e70-87ed-7e94cede0858.png)


For reviewed implementation:

![图片](https://user-images.githubusercontent.com/57332517/155641442-b945d167-0b16-40d6-80c4-6a4dc007a62d.png)

My implementation has index out of bound. I think it is because I did not check whether nextOpenBracket is 0, so 0 - 1 will have index out of bound.
Overall, I think it will be about MORE than 10 lines for my implementation to make the change, so it can be like: 1. check the "0" for the variable to avoid index out of bound 2. Try to have a if-statement to check whether there is additional brackets between brackets or addtional parentheses between parentheses. When they have addtional matched ones, the code should continue to add those links with bracket or parentheses but not just break and jump to next link. 


### Snippet 3

Should be:

![图片](https://user-images.githubusercontent.com/57332517/155643836-61083d5f-9e51-46ef-b089-eb37024bc400.png)

Test in VScode:

![图片](https://user-images.githubusercontent.com/57332517/155644098-6002727d-0973-4b19-baef-f7c50d3d2a90.png)

For my implementation:

![图片](https://user-images.githubusercontent.com/57332517/155644872-2c64a9e7-c123-4e8e-970b-757745892ac7.png)


For review implementation:

![图片](https://user-images.githubusercontent.com/57332517/155644190-8a850e87-640c-44d1-b152-0e4f364f330e.png)

The error for me is index out of bound which should at when nextOpenBracket equals 0, so this can be finished real quick. Rest of the error is:

![图片](https://user-images.githubusercontent.com/57332517/155645131-30fdbddc-5b5c-4700-9f37-5e8dd83a0d21.png)

Which tells me: 1. I need to check the closing parenthesis in the loop. When there is no closing, the link should be invalid. 2. If there is no closing, and next bracket comes, the code should be able to discard the previous link and begin with another bracket check since the next link may be valid. 3. The code needs to check if the link has a adjacent closing parenthesis within two lines. Because if the closing parenthesis comes after two new lines in markdown like `(link.com \n \n)`, the link is invalid.


Thank you for reading.
