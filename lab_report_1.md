# Lab Report 1
How to remotely login to CSE basement servers through VSCode.**  

**Setting the password** 
1. Go to the [UCSD course account lookup tool](https://sdacs.ucsd.edu/~icc/index.php)   
    ![Course account lookup image](\cse15l-lab-reports\img\lookup.png)
2. Enter your username and PID
3. Select your course account, this should be the one that starts with a cse15lwi23  
    ![course account](\cse15l-lab-reports\img\course_account.png)
4. Select the change your password option
5. Enter your new password and finish resetting your password.  
    ![password reset](\cse15l-lab-reports\img\password.png)  
    
**Downloading VSCode**
1. Go to [VSCode download page](https://code.visualstudio.com/download)  
    ![vscode download](\cse15l-lab-reports\img\download2.png)  
2. Select the right download option for your computer to download the installation file
3. Click on the exe file and follow all installation instructions.
4. Open VsCode and select "Run Terminal" in the Terminal menu of the top toolbar.  
    ![terminal](\cse15l-lab-reports\img\select_terminal.png)  
    
**Accessing the Server**
1. In your terminal enter `$ ssh <course_account_name>@ieng6.ucsd.edu`  
   If you've never logged in before, you should see something like 
    ```
    -> ssh cs15lwi23zz@ieng6.ucsd.edu 
    The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established. 
    RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec. 
    Are you sure you want to continue connecting (yes/no/[fingerprint])? 
    ```
2. Enter yes, then your password. Note that your password will not be visible as you're typing it.
3. If you see 
    ```
    # Now on remote server
    Last login: Sun Jan  2 14:03:05 2022 from 107-217-10-235.lightspeed.sndgca.sbcglobal.net
    quota: No filesystem specified.
    Hello cs15lwi23zz, you are currently logged into ieng6-203.ucsd.edu

    You are using 0% CPU on this system

    Cluster Status 
    Hostname     Time    #Users  Load  Averages  
    ieng6-201   23:25:01   0  0.08,  0.17,  0.11
    ieng6-202   23:25:01   1  0.09,  0.15,  0.11
    ieng6-203   23:25:01   1  0.08,  0.15,  0.11

    Sun Jan 02, 2022 11:28pm - Prepping cs15lwi23
    ```
    Congrats, you've successfully logged in to the server.
