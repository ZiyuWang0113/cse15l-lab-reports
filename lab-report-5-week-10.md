# CSE 15L Lab Report-4-week8

## Ziyu Wang ziw003@ucsd.edu

1. Copy the test-files and script to my markdown and output the result.

![图片](https://user-images.githubusercontent.com/57332517/157772057-00f2b728-125d-44ad-b56a-6194959b0bc3.png)

2. I used `diff` to find difference between two txt files(the results of for-loop bash). And here is an Overview.

![图片](https://user-images.githubusercontent.com/57332517/157773393-724228fa-3a0a-4b89-96cf-6fa43c13fc77.png)

3. **For files that have very similar output difference, I will say refer to #(num) of test since they should be fixed with a similar approach.**

#1. Test 194

![图片](https://user-images.githubusercontent.com/57332517/157774565-a9778f03-381a-4e57-a5c4-11b0526895dc.png)


I would say my output seems more correct since the "url" is not a link, it is only a word with underline. The bug is that this word is behind bracket and it is inside one complete block but there are something between bracket and parentheses , so the code may consider it as a valid link. I think the fix should first check whether the bracket is matched, and then check the parentheses is right after a valid pair of bracket(which is failed, thus select the word url out(inside a parentheses)).

#2. Test 201

![图片](https://user-images.githubusercontent.com/57332517/157774592-62331cf4-2b83-4919-b273-868a06b79453.png)

Similar to #1 Test 194, which has other words between bracket and parentheses, also the parentheses. So similar fix solution as Test 194.

#3.
