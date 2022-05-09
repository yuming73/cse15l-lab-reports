# [CSE 15L Lab Report 3](https://yuming73.github.io/cse15l-lab-reports/lab-report-3-week-6.html)    
## Group Choice Options From Lab 5    

### Option 1- Streamlinging ssh Configuration    
1. Create a `.ssh/config` file using the command `vim ~/.ssh/config` in the terminal. The file should contain the hostname and the user of the remote host `ieng6`. To save the file after editing, click on the `esc` button and type `:wq`, which means to save and exit the editor.   
![.ssh/config file](lab5_screenshot1.png)   
2. We should now be able to log onto the `ieng6` remote server just by using the command `ssh ieng6`, in which case the `ieng6` is a shortened alias for our account name.  
![ssh command](lab5_screenshot2.png)   
3. We can also use the `scp` command to copy files to the remote account with just the `ieng6` alias.    
![scp command](lab5_screenshot3.png)   

---   

### Option 2- Setup Github Access From ieng6   
1.   
![public key on Github](lab5_screenshot4.png)   
2.    
![log onto on ieng6](lab5_screenshot5.png)   
![create public key on ieng6](lab5_screenshot6.png)   
![location of public and private key on ieng6](lab5_screenshot7.png)   
3.   
![commit and push on ieng6](lab5_screenshot8.png)   
4. [link](https://github.com/yuming73/Skill-Demonstration/commit/b6717595e1d39a08ccb34328da57c4a85263d700) [link2](https://github.com/yuming73/Skill-Demonstration/commit/b6717595e1d39a08ccb34328da57c4a85263d700)   
   
---   

### Option 3- Copy Whole Directories With `scp -r`   
1.    
![copy to ieng6](lab5_screenshot9.png)   
2.    
![confirm in ieng6](lab5_screenshot10.png)   
3.   
![compile and run](lab5_screenshot12.png)   
4.   
![](lab5_screenshot13.png)   
![](lab5_screenshot14.png)   
![](lab5_screenshot15.png)   

---   