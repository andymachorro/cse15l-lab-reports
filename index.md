# Lab 3 Part 1:
### SSH Config File
- For the first step, I make a config file by making an .ssh file, and pasting the following contents shown in the file
<img width="1440" alt="Screen Shot 2022-05-10 at 6 04 58 PM" src="https://user-images.githubusercontent.com/103210240/167749549-360982b8-1950-48aa-bf35-abb10315684e.png">

- The script shown above allows us to configure a way to make accessing our ieng6 accounts much eaiser by using the following command:
```
ssh ieng6
```

<img width="1440" alt="Screen Shot 2022-05-10 at 6 50 17 PM" src="https://user-images.githubusercontent.com/103210240/167752623-c1774cbb-d954-4b29-90c0-db79ed211257.png">

- In the image above, I copied a newly created file newFile.java, onto the ieng6 server using the following command:
```
scp newFile.java ssh ieng6:~/
```


# Lab 3 Part 2:
### Stored in User Account
![image](https://user-images.githubusercontent.com/103210240/167986684-6da1918d-d56a-4570-ad77-f3541efe0a95.png)


- The image above demonstrates where the ssh public key can be found, I then copied this and pasted it onto the Github page for ssh keys

### Stored on Github
![image](https://user-images.githubusercontent.com/103210240/167983475-ba794d45-3f05-4fac-8cb8-94ec70c98d6b.png)

- This key was generated from the ieng6 server and was copied from the terminal, I then pasted the ssh public key onto the Github ssh-keys holder. This key is now stored onto my github account


![image](https://user-images.githubusercontent.com/103210240/167983673-a311dc34-c6a2-4907-97f3-98f915e0291d.png)

- In the photo demonstrated above, my private key is stored into .ssh folder, which is retrieved by loading the hidden files from my User account

![image](https://user-images.githubusercontent.com/103210240/167993277-85d96914-8f24-4bd9-a493-e295f529a393.png)

- In the image above, I use the following commands to commit and push my file MarkdownParse2.java onto github, all while doing so in the ieng6 server


# Lab 3 Part 3:
### Copying/Pasting directories onto ieng6 server

![image](https://user-images.githubusercontent.com/103210240/167985633-d035f762-f6e0-4563-a341-e3df16c414ad.png)

- In the image above, I was able to copy my entire directory from my local server, onto the ieng6 server using the following command:
```
scp -r . cs15lsp22aot@ieng6.ucsd.edu:~/markdown-parse
```


<img width="1440" alt="Screen Shot 2022-05-10 at 6 41 20 PM" src="https://user-images.githubusercontent.com/103210240/167751804-ac611d51-5f7b-41ad-805b-251222c3946a.png">

- In the image shown above, I ran the tests that were found in the MarkdownParseTest.java, making sure that it would complie and run, and it did run successfully
