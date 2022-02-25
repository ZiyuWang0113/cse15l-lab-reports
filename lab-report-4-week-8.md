# CSE 15L Lab Report-4-week8

## Ziyu Wang ziw003@ucsd.edu

Link to my repository: [My](https://github.com/ZiyuWang0113/markdown-parse-new)

Link to reviewed repository: [Reviewed](https://github.com/kathyychenn/markdown-parse)

### Snippet 1

Should be: ![图片](https://user-images.githubusercontent.com/57332517/155637710-5cc31f6c-de1c-42fa-a4a1-7efa370f38b6.png)

Test in VScode:
![图片](https://user-images.githubusercontent.com/57332517/155638527-68627d84-de88-4e6f-8bb9-90f4aabae245.png)

For my implementation:
![图片](https://user-images.githubusercontent.com/57332517/155639450-a77040d5-d50a-492e-b9b9-6ff6584d4ca5.png)

I think there can be a small code change to fix it. It should check the \` between brackets so when there are two of them, the characters turn into a code block. So, maybe create new variables to trace the locations for \`, and then check whether the brackets still work. In the parentheses， the \` can be igored since the parentheses has higher priority so the link will be kept. I would say 10 line is roughly enough.

For reviewed implementation:
![图片](https://user-images.githubusercontent.com/57332517/155638678-0c8d9027-226b-41a2-8d9a-3663aac2161c.png)

I think there can be a small code change to fix it. It should check the \` between bracket so when there are two of them, the characters turn into a code block. So, maybe create a new varibale to trace the location for \`, and then check whether the brackets still work. In the parentheses， the \` can be igored since the parentheses has higher priority so the link will be kept. I would say 10 line is roughly enough.
