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

#3. Test 22

![图片](https://user-images.githubusercontent.com/57332517/157774738-142e78f3-21e5-4240-a354-291d57d17f14.png)

I think both output is wrong. However, I am not sure for this test file, I would say the correct output is the link "bar*" if the markdown is generated. If my expected output is correct, I would say the fix need to check the quotes between the valid parentheses since the words in the quotes is the document and do not count as link itself. So, check quotes in valid parentheses is required.

#4. Test 32

![图片](https://user-images.githubusercontent.com/57332517/157775277-9f177180-a796-425f-85cf-551d8c0b2de9.png)
 
I think my output is wrong. This is not a valid link, so the output should be empty. It's similar to #3 Test 22 since the quote check is required, also, links usually are without special punctuations.

#5. Test 41

![图片](https://user-images.githubusercontent.com/57332517/157775621-cf288cc9-52e5-47be-a581-725276b673c2.png)

I think my output is wrong. This is not a valid link, so the output should be empty. Similar to Test 22 and Test 32.

#6. Test 481

![图片](https://user-images.githubusercontent.com/57332517/157777088-9f340c73-fe8b-4b3d-9e68-6dc964f49e9b.png)

Similar to Test 22, the quote check.

#7. Test 487

![图片](https://user-images.githubusercontent.com/57332517/157778202-05d75d5b-6cf6-4a55-8162-b9811b2ba18b.png)

I think my output is wrong. The expected output should be empty since there is a slash, so it is similar to the quote check, the slash should also be checked inside the parentheses.

#8. Test 488

Similar to Test 487

#9 Test 489

![图片](https://user-images.githubusercontent.com/57332517/157779754-6bb4b4c3-e0dd-4c1e-969b-7644480307fa.png)

I think my output is wrong. Since this is a new line, it is not a valid link. In my code, I should check the `\n` which will influence the link. The fix should be about to check the `\n` inside a valid parentheses after bracket.





