## Lab Report 4

4. Log into ieng6  
![image](https://user-images.githubusercontent.com/73797155/221445942-3febf44d-1ced-461b-bd56-d2c98a5077a0.png)  
Keys pressed: `<up><enter>`  
The `ssh cs15lwi23aqx@ieng6.ucsd.edu` command was 1 up in the history, so I simply accessed it using up arrow.

5-7 Clone your fork of the repository from your Github account, Run the tests, demonstrating that they fail and Edit the code  
![image](https://user-images.githubusercontent.com/73797155/221446523-4fed5467-1e44-460a-9814-377738f14d4c.png)  
![image](https://user-images.githubusercontent.com/73797155/221446714-23ee7ccc-70e2-4013-b431-0542a9bd507e.png)  

Keys pressed: `<up><up><up><up><enter><ctrl+shft+->43<enter>(<right>x11)<del>2<ctrl+x>y<enter>`  
The ```git clone git@github.com:maxwn04/lab7.git; cd lab7; cd lab7; javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java; java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples; nano ListExamples.java```
command was 4 up in the history, so I accessed it using the up arrow. This command contains all the commands needed for steps 5-7, first cloning the github, then 
switching into the folder and running the junit compile and run commands. Then using nano to edit the file. I used the ctrl+shft+- shortcut to skip to line 43, 
then used the right arrow to get to the error, and fixed it by deleting the 2 and replacing it with a 1.  

8-9 Run the tests, demonstrating that they now succeed and Commit and push the resulting change to your Github account  
![image](https://user-images.githubusercontent.com/73797155/221446951-510ae494-6b0a-4faa-82b3-07f97ab54e69.png)  

Keys pressed: `<up><up><up><up><enter>`  
The ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java; java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples; git add ListExamples.java; git commit -m "Updated"; git push origin main```
command was 4 up in the history, so I accessed it using the up arrow. This command contains all the commands needed for steps 8-9, first running the Junit compile and run
commands, then running all the required commands to push the changes to github.
