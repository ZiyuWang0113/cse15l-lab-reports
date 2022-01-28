# CSE 15L Lab Report-2-week4

## Ziyu Wang ziw003@ucsd.edu

### 1

Code:

![Image](https://user-images.githubusercontent.com/57332517/151465024-b5903e80-a4ea-4a03-b81b-96327159e3d9.png)

The link to the file which has the related error: [test-file2](https://github.com/ZiyuWang0113/markdown-parse/blob/main/test-file2.md). In the file, the brackets are incorrect.

The incorrect terminal output in local computer:

![Image](https://user-images.githubusercontent.com/57332517/151465737-26139b36-fdf0-4d3a-b763-95bcfdccfb7f.png)

The bug is because the code did not handle the situation when the brackets are not matched(only has one side or has incorrect form).
When we compile and run the code, the symptom is shown as `StringIndexOutOfBoundsException: at java.base/java.lang.String.checkBoundsBeginEnd(String.java:4601)`, this is
because when we search for next bracket, there is no result, so Java will have index error.

Everytime if java has some error with index, we should consider whether we handle some extreme case about missing or wrong format.



### 2

Code:

![Image](https://user-images.githubusercontent.com/57332517/151467609-b7cfb09d-0b45-4780-b777-16c59a776a56.png)

The link to the file which has the related error: [test-file3](https://github.com/ZiyuWang0113/markdown-parse/edit/main/test-file3.md)

The incorrect terminal output in local computer:

![Image](https://user-images.githubusercontent.com/57332517/151467473-1c14334a-3995-41d8-a4e9-e7d9d4dcc1cb.png)

This bug is because the code did not end the search when there is no more brackets in the markdown.
When we compile and run the code, the symptom is shown as printing the same value infinitely (infinite loop), this is because when there is no more bracket,
the program did not end in time but continued to run forever.

Everytime if java has an infinite running, we should consider we wrote something in recursion or loop with an infinite syntax.



### 3

Code:

![Image](https://user-images.githubusercontent.com/57332517/151469472-32f61c2b-1f33-47ae-ac85-646259cd451d.png)

The link to the file which has the related error: [test-file4](https://github.com/ZiyuWang0113/markdown-parse/blob/main/test-file4.md)

The incorrect terminal output in local computer:

![Image](https://user-images.githubusercontent.com/57332517/151470894-0b2715cc-3419-4ee6-994b-0b9870c42182.png)

This bug is because the code did not find the image link correct and consider it as incorrect. When we compile and run the code, the symptom is shown as it outputs the correct link before the image twice, which indicates the code did not find the correct link for image.

Everytime if java has incorrect output about some contents which were corrected designed before this input, we should be aware of those new-comming inputs, try to make sure we separate them and handle with different situations.


