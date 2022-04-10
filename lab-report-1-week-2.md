# [CSE 15L Lab Report 1](https://yuming73.github.io/cse15l-lab-reports/lab-report-1-week-2.html)  
## How To Log Into A Course-Specific Account On `ieng6`     
    
**Step 1**   
[**Download Visual Studio Code**](https://code.visualstudio.com/)    
![installing vscode](lab1_screenshot1.png)    

---

**Step 2**   
**Remotely Connecting**  
*Prestep For Microsoft Users: [Install OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)*    
*Look Up Course Specific Account: [Here](https://sdacs.ucsd.edu/~icc/index.php)*    
1. Open a terminal in VSCode and run the command: `$ ssh cs15lsp22zz@ieng6.ucsd.edu` (replaced *`zz`* with the last three letters in your course specific account)  
2. Say yes to the "*Are you sure you want to continue connecting*" messages if connecting to the server for the first time  
3. Provide your password and the terminal should look something similar to this to indicate that you are logged in:  
![remotely connecting](lab1_screenshot3.png)   

---

**Step 3**  
**Trying Some Commands**    
Here's a list of suggestions of commands to try out:
* `cd ~` ()
* `cd` ()
* `ls -lat` ()
* `ls -a` ()
* `ls <directory>` ()
* Ctrl-D or `exit` (logs you out of the remote server in the terminal)
* `cp /home/linux/ieng6/cs15lsp22/public/hello.txt ~/` ()  
* `cat /home/linux/ieng6/cs15lsp22/public/hello.txt` ()    

When trying the last two commands, you might encounter something like this:   
![trying some commands](lab1_screenshot4.png)  
This means ()   

---

**Step 4**  
**Moving Files With `scp`**   
1. Create a file on your computer called `WhereAmI.java` with the following contents:
```
class WhereAmI {
    public static void main(String[] args) {
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
}
```
2. In the directory of the file, run the command: `scp WhereAmI.java cs15lsp22zz@ieng6.ucsd.edu:~/` (replaced *`zz`* with the last three letters in your course specific account) and provide your password
3. Log into `ieng6` with `ssh` and run the `ls` command to check that the file has successfully been copied
4. The terminal should look similar to this in this process:   
![moving files with scp](lab1_screenshot2.png)    
![moving files with scp](lab1_screenshot5.png)    
5. You can use `javac` and `java` to observe the difference between the outputs from running on the client (local computer) vs. running on the server (remote server)   

---

**Step 5**   
**Setting an SSH Key**    
1. On the client (local computer), run the command: `ssh-keygen`, **do not add a passphrase for this step**
2. Log into `ieng6` with `ssh` and copy the public key to the `.ssh` directory of your user account on the server with the command: `mkdir .ssh`   
3. Log out of the server and on client, run the command: `scp /Users/<user-name>/.ssh/id_rsa.pub cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys` (replaced with your username)
4. When prompt to select a path, use the path you saw in the command above   
5. You should now be able to log into `ieng6` without a password, with a terminal similar to this:  
![remote login without password](lab1_screenshot6.png)   

---

**Step 6**   
**Optimizing Remote Running**   
