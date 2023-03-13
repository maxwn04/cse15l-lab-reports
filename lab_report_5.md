## Lab Report 5

### Doing commands quickly with bash scripts.

For lab report 4, instead of having a couple very long commands, we could actually have made it much faster by simply using a bash script. To do this simply copy all of the commands used for the tasks into a bash script. However, instead of using `nano` we will use the `sed` command to edit the file.  
![image](https://user-images.githubusercontent.com/73797155/224789695-4610f7c2-63e1-499c-9fbf-4372a1b14107.png)  
As seen on line 5, we are using `sed -i '43s/index1 += 1/index2 += 1/g' ListExamples.java` instead of `nano`.  
The `-i` option allows the command to edit the file in place, rather than simply printing the edited file.  
The `'43s/index1 += 1/index2 += 1/g'` tells the command to look in line 43, and replace `index1 += 1` with `index2 += 1` which fixes the bug.  

After creating the script copy the command to the server using `scp`
`scp fast.sh cs15lwi23aqx@ieng6.ucsd.edu:`  
![image](https://user-images.githubusercontent.com/73797155/224580113-2c1fe5de-12bb-4a93-9ec8-a49e339d9e2c.png)


Then ssh to the server  
![image](https://user-images.githubusercontent.com/73797155/224580126-4bb9d215-bf41-412d-8e2b-46233d77a083.png)  

And run the bash script using `bash fast.sh` which gives the output below  
```
Cloning into 'lab7'...
JUnit version 4.13.2
..E
Time: 0.889
There was 1 failure:
1) testMerge2(ListExamplesTests)
org.junit.runners.model.TestTimedOutException: test timed out after 500 milliseconds
        at java.util.Arrays.copyOf(Arrays.java:3210)
        at java.util.Arrays.copyOf(Arrays.java:3181)
        at java.util.ArrayList.grow(ArrayList.java:267)
        at java.util.ArrayList.ensureExplicitCapacity(ArrayList.java:241)
        at java.util.ArrayList.ensureCapacityInternal(ArrayList.java:233)
        at java.util.ArrayList.add(ArrayList.java:464)
        at ListExamples.merge(ListExamples.java:42)
        at ListExamplesTests.testMerge2(ListExamplesTests.java:19)

FAILURES!!!
Tests run: 2,  Failures: 1

-bash: line 8: cd: lab7/: No such file or directory
JUnit version 4.13.2
..
Time: 0.016

OK (2 tests)

[main 4973aa1] edit file
 Committer: Max Weng <cs15lwi23aqx@ieng6-203.ucsd.edu>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 1 file changed, 1 insertion(+), 1 deletion(-)
To github.com:maxwn04/lab7.git
   f750e52..4973aa1  main -> main
```
Which shows all the steps being executed correctly.
