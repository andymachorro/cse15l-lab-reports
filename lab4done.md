# Lab Report 4

## Common Mark Code Preview ##
![image](https://user-images.githubusercontent.com/103210240/169740904-a7a56aac-aee9-4e36-a622-34650ef29108.png)

![image](https://user-images.githubusercontent.com/103210240/169740773-4be7338e-799a-4793-842d-0d97a3d70094.png)

![image](https://user-images.githubusercontent.com/103210240/169741006-fca2fb44-bcf1-4d47-b477-0ef4bbeaf0d7.png)









## Test Implementations Using J-Unit ##
![image](https://user-images.githubusercontent.com/103210240/169678935-2de24d20-804d-409e-ac07-e4011a5d99c4.png)
![image](https://user-images.githubusercontent.com/103210240/169679055-da508cef-c903-4da7-b84a-38b30c7c29c2.png)







## My Tests ##
### Snippet 1 (PASSED) ###
- This test passed due to the fact that I inserted a the links for the test, which consisted of url.com, `google.com, google.com and ucsd.edu.
### Snippet 2 (FAILED) ###
![image](https://user-images.githubusercontent.com/103210240/169679190-9094ac2e-a2b7-4973-81f9-22dc04d64eb9.png)
### Snippet 3 (Failed) ###
![image](https://user-images.githubusercontent.com/103210240/169679228-1b171726-b09e-43be-a792-ae4e1dda224d.png)


## Their Errors ##
### Snippet 1 (Failed) ###
![image](https://user-images.githubusercontent.com/103210240/169679173-c43e2d3b-5588-47ed-9817-32c606c973dc.png)
### Snippet 2 (Failed) ###
![image](https://user-images.githubusercontent.com/103210240/169679261-74f48ba0-c42b-4a5e-980a-f06c5025fd29.png)
### Snippet 3 (Failed) ###
![image](https://user-images.githubusercontent.com/103210240/169679277-e9fff3d0-a2a2-443d-8a69-dc0b130c867e.png)


## Conclusion (for Both Versions) ##
### Snippet 1 ###
- My version of MarkdownParse.java passed the first code snippet because we made sure to only allocate the closing points of the brackets and parenthesis. We started the while loop with an indexOf([, currentIndex), making sure it starts with the bracket, then parenthesis.
- Their version of MarkdownParse.java failed the first test because of the fact that it didn't read the last link, that being ucsd.edu. This would probably be a more involved change due to the fact that the conditional statement would have to be changed to run for as long as it isn't -1. This would be more suitable in this case, as the length can become tricky with empty spaces, with this stated however, it does take into consideration the backticks.

### Snippet 2 ###
- My version of MarkdownParse.java failed the second code snippet as it read the last part of the code, that being example.com, and it read the middle link as a.com((. It works with parenthesis and brackets for the most part, execpet fot escaped brackets. I think this will be an easy fix as all it requires is an if statement that will only check for brackets at a time. If statements for every single sceneario.
- Their version of MarkdownParse.java failed the second part as well and did not take into consideration the example.com link. This could be a lengthy code change as it would have to count and keep track of the amount of brackets and parenthesis it encounters.

### Snippet 3 ###
- My version of MarkdownParse.java failed the third code snippet as my test couldn't make any newlines, however, the result seemed to consider the new lines when retrieving the links. I believe this could be resolved if I check the amount of newline space there is in the String arraylist created.
- Their version of MarkdownParse.java failed the third code snippet for the same reason as mine. This could also be resolved within a less than ten lines as all it would need is an if statement checking the amount of blank space found inside the string added into the arraylist.
