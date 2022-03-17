# CSE 15L Lab Report-5-week10

## Ziyu Wang ziw003@ucsd.edu

**Code Naviagtion problem for Test 22, 489, 571 (three main problems, others are similar)fixed. Code screenshots updated, also provided place to add NEW conditional checks.**

A. Copy the test-files and script to my markdown and output the result.

![图片](https://user-images.githubusercontent.com/57332517/157772057-00f2b728-125d-44ad-b56a-6194959b0bc3.png)

B. I used `diff` to find difference between two txt files(the results of for-loop bash). And here is an Overview.

![图片](https://user-images.githubusercontent.com/57332517/157773393-724228fa-3a0a-4b89-96cf-6fa43c13fc77.png)

C. **For files that have very similar output difference, I will say refer to #(num) of test since they should be fixed with a similar approach.**

#1. Test 194

![图片](https://user-images.githubusercontent.com/57332517/157774565-a9778f03-381a-4e57-a5c4-11b0526895dc.png)


I would say my output seems more correct since the "url" is not a link, it is only a word with underline. The bug is that this word is behind bracket and it is inside one complete block but there are something between bracket and parentheses , so the code may consider it as a valid link. I think the fix should to add check statements to first check whether the bracket is matched, and then check the parentheses is right after a valid pair of bracket(which is failed, thus select the word url out(inside a parentheses)).

#2. Test 201

![图片](https://user-images.githubusercontent.com/57332517/157774592-62331cf4-2b83-4919-b273-868a06b79453.png)

Similar to #1 Test 194, which has other words between bracket and parentheses, also the parentheses. So similar fix solution as Test 194.

#3. Test 22

![图片](https://user-images.githubusercontent.com/57332517/157774738-142e78f3-21e5-4240-a354-291d57d17f14.png)

I think both output is wrong. However, I am not sure for this test file, I would say the correct output is the link "bar*" if the markdown is generated. If my expected output is correct, I would say the fix need to add the check the quotes between the valid parentheses since the words in the quotes is the document and do not count as link itself. So, check quotes in valid parentheses is required.

Which code should be fixed:

![图片](https://user-images.githubusercontent.com/57332517/158759533-2b1c3eb6-5d69-4b18-9f3f-0a9d4569e5be.png)

When there is just bracket check, those documented words are not checked, and this will cause an error since this code just include everything in the parentheses. So before ending this while loop, in the if statements, there should be a qutoe check right after the bracket is qualified.

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

#9. Test 489

![图片](https://user-images.githubusercontent.com/57332517/157779754-6bb4b4c3-e0dd-4c1e-969b-7644480307fa.png)

I think my output is wrong. Since this is a new line, it is not a valid link. In my code, I should add to check the `\n` which will influence the link. The fix should be about to check the `\n` inside a valid parentheses after bracket.

Which code should be fixed:

![图片](https://user-images.githubusercontent.com/57332517/158760128-5cd648f0-7d44-461e-835a-7c73e13d7098.png)

The wrong code is that it missed the check about "\n" so it will consider everything including a new line between parentheses, so after checking those missing parentheses, in the if statements, we need to add a "\n" check that if \n is detected, do not put contents as link and skip the index to next closed parentheses.

#10. Test 490

![图片](https://user-images.githubusercontent.com/57332517/157780028-d34a96ff-c3d8-4795-aee0-20f679423cab.png)

Exact issue with Test 489, but also with the `<>`.

#11. Test 494

![图片](https://user-images.githubusercontent.com/57332517/157780203-3315b14e-34f6-46a5-b39f-1242e67c6372.png)

I think my output is wrong. Since there is another parentheses inside the valid ones, the expected output should be the link with complete parentheses.The fixed should add to check if there is nested parentheses inside, and match the number of them, which can help to get those inner ones out aftre we reach the last close parentheses.

#12. Test 495

![图片](https://user-images.githubusercontent.com/57332517/157780215-4960d3bc-8949-40e1-95ee-62e530f06003.png)

Exact same issue with Test 494, to add a check in code to check inner parentheses.

#13. Test 498

![图片](https://user-images.githubusercontent.com/57332517/157780801-6beddbca-93b2-4d84-b932-221a34af889c.png)

Same issue with Test, but more with the `<>`. So the fix should also check whether these lines are in a block of <>.

#14. Test 505

![图片](https://user-images.githubusercontent.com/57332517/157781016-9a775dc6-a588-4352-af31-6f063b1a2d45.png)

I think both are wrong. Since there are quotes, so the expected output is just the give url. The fix is similar to Test 32 which adds a quote check inside parentheses.

#15. Test 506, 507, 508, 509

All issues with url and quotes. My code is incorrect obviously. The general fix is to add a first check about `/url`, and then chech the quotes, so if both are satisfied, we can keep that link in the parentheses.

#16. Test 510

![图片](https://user-images.githubusercontent.com/57332517/157781912-e7701f64-44dc-4225-a6d4-41595b5545a2.png)

I think prof's output is wrong. Since it is only a url, the link is not valid, the output should be empty. The fix is to add a additional if-statement to check whether a url in only url inside a parentheses, which will not be valid to form a link.

#17. Test 511

![图片](https://user-images.githubusercontent.com/57332517/157782144-abf5afa8-d1f6-450b-9eec-55c3095d5ad1.png)

I think my output is wrong. Since the url is correct, but there is more nested bracket inside bracket. So the fix should also add another check to check nested bracket, which is simialr to check nested parentheses inside parentheses.

#18. Test 567

![图片](https://user-images.githubusercontent.com/57332517/157783586-3019fad2-615c-458a-9bf2-e2851d6fe2ec.png)

Both outputs are wrong since the "not a link" is not a link. The true link is the url1. So the fix should be to add additional check to check whether there is a colon after this link which will assgian a new address link to it. So we need a if-statement after this bracket to check a colon, and if a colon gives a link, we need to use this link to replace.

#19. Test 571

![图片](https://user-images.githubusercontent.com/57332517/157784162-9acd1272-ac08-48da-91aa-48c611966324.png)

My output is wrong. Since it starts with an `!`, so it is a image, we do not consider it as link, the output should be empty. For fix, I need to add a check about exclamation mark before the open bracket. If there is a `!`, we should skip the next parentheses which is a image.

which code should be fixed:

![图片](https://user-images.githubusercontent.com/57332517/158760628-9a11b52b-77b6-443b-b83d-be9529f55e87.png)

The code did not check an `!` for an image, so for current loop, it will mistakely take everything between parentheses even if it's a link. So before the nested two if statements, if there is an `!` before bracket, we should set current index to the next closed parentheses and use continue to skip current loop.

#20 Test 578

![图片](https://user-images.githubusercontent.com/57332517/157784437-658dc2a0-14f1-4b4f-ada8-5a430f8d51ce.png)

Same issue with Test 571 about image. The fix should check `!` and skip the next parentheses block if it is image. Furthermore, the quote is also here, so similar to Test 32, a quote check is also helpful.


**Thank you for reading.**
