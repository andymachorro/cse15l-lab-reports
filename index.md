# Remote Access
### We will be showing you how to access your course-specific ieng6 account!
**1. Install VS Code (Visual Studio Code)**
<img width="1440" alt="Screen Shot 2022-03-31 at 10 19 45 AM" src="https://user-images.githubusercontent.com/103210240/162271535-0da253e8-cb4f-4928-aa71-ff074483647e.png">

Visit [VSCode](https://code.visualstudio.com/) and following instructions to download and install it on your computer. There are versions for all the major operating systems, like OSX (for Macs) and Windows (for PCs), so it is important to identify your operating system.

**2. Remotely Connecting** 
<img width="1440" alt="Screen Shot 2022-04-06 at 10 57 45 PM" src="https://user-images.githubusercontent.com/103210240/162273289-b561ef49-fa99-4973-bcbc-ae288889a5ac.png">

For Window users, make sure to install **OpenSSH**. To remotely connect your device, you will need to visit your course-specific account for CSE15L [here](https://sdacs.ucsd.edu/~icc/index.php) to access your course specific information. For the first step, open a terminal in VSCode (Ctrl or Command + `, or use the Terminal → New Terminal menu option). Your command will look like this, but with the zz replaced by the
letters in your course-specific account.
<br>
**$ ssh cs15lwi22zz@ieng6.ucsd.edux**
<br>
(That’s one, five, l (not one); the one and l look very close in some fonts.)

**3. Trying Some Commands** 
Try running the commands: ***cp***,
                          ***ls***,
                          ***pwd***,
                          ***mkdir***,
  ***scp***
  
  <img width="1440" alt="Screen Shot 2022-03-31 at 11 26 43 AM" src="https://user-images.githubusercontent.com/103210240/162528558-c1a24cfc-fa31-4661-b589-9a620d846746.png">
  
  Make sure to open the terminal found in VS Code. Try using the commands listed above, one at a time.
  
  **4. Moving Files with scp**
  
Now, we are going to copy a file (more many files) from your computer to a remote computer. This command is formally known as the ***scp*** command, and we will always run it from the client (that means from your computer, not logged into ieng6). Create a file on your computer called WhereAmI.java and put the following contents into it:
<br>
<br>
 **class WhereAmI {
 <br>
  public static void main(String[] args) {
  <br>
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
}**

Run it using javac and java on your computer.
Then, in the terminal from the directory where you made this file, run this command (as usually, using your username):
<br>
**scp WhereAmI.java cs15lwi22zz@ieng6.ucsd.edu:~/**
<br>
You should be prompted for a password just like when you log in with ssh.

<img width="1440" alt="Screen Shot 2022-04-09 at 6 52 57 PM" src="https://user-images.githubusercontent.com/103210240/162598463-b43c22e9-b569-4765-ab81-71da1e6c78e9.png">

Then, log into ieng6 with ssh again, and use ls. You should see the file there in your home directory! Now you can run it on the ieng6 computer using javac and java. Since java is installed on the server, everyone should be able to run it no matter the client.

<img width="1440" alt="Screen Shot 2022-04-09 at 6 56 48 PM" src="https://user-images.githubusercontent.com/103210240/162598468-fa584d63-f596-46dc-9b8d-0a41fd343a71.png">

**5. Setting an SSH Key**

The idea behind ssh keys is that a program, called ssh-keygen, creates a pair of files called the public key and private key. You copy the public key to a particular location on the server, and the private key in a particular location on the client. Then, the ssh command can use the pair of files in place of your password. This is a common setup step in lots of work environments that involve code on a server.


<img width="1440" alt="Screen Shot 2022-04-09 at 8 47 53 PM" src="https://user-images.githubusercontent.com/103210240/162600661-ae227164-de47-47c1-a598-26d25a1afe69.png">

This created two new files on your system; the private key (in a file id_rsa) and the public key (in a file id_rsa.pub), stored in the .ssh directory on your computer.
Now we need to copy the public (not the private) key to the .ssh directory of your user account on the server.


<img width="1440" alt="Screen Shot 2022-04-09 at 8 46 31 PM" src="https://user-images.githubusercontent.com/103210240/162600680-4c26d70f-07b6-42c3-b27d-e2d3f38efa96.png">

**6. Optimizing Remote Running**
Now that we know this information, we can efficiently copy/edit files onto a remote server, and run it.
Some hints: 
- You can write a command in quotes at the end if an ssh.
- You can use semicolons to run multiple commands on the same line in most terminals. 

For example, try:
$ cp WhereAmI.java OtherMain.java; javac OtherMain.java;
java WhereAmI

Try to get the total time for a run after editing and saving to under 10 total keystrokes/mouse clicks, including all typing.
If you have more time, brainstorm other ideas or search for other ways you might easily run remote code.

![Screen Shot 2022-04-10 at 8 39 16 PM](https://user-images.githubusercontent.com/103210240/162661406-507b3f12-d614-4ab7-81af-9a416ac446b6.png)

