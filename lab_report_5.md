## Lab Report 5

### Doing commands quickly with bash scripts.

For lab report 4, instead of having a couple very long commands, we could actually have made it much faster by simply using a bash script. To do this simply copy all of the commands used for the tasks into a bash script. However, instead of using `nano` we will use the `sed` command to edit the file.  
![image](https://user-images.githubusercontent.com/73797155/224580157-88fbffdb-fc82-44da-a061-8441424bb7fb.png)  
As seen on line 5, we are using `sed -i '43s/index1 += 1/index2 += 1/g' ListExamples.java` instead of `nano`.  
The `-i` option allows the command to edit the file in place, rather than simply printing the edited file.  
The `'43s/index1 += 1/index2 += 1/g'` tells the command to look in line 43, and replace `index1 += 1` with `index2 += 1` which fixes the bug.  

After creating the script copy the command to the server using `scp`
`scp fast.sh cs15lwi23aqx@ieng6.ucsd.edu:`  
![image](https://user-images.githubusercontent.com/73797155/224580113-2c1fe5de-12bb-4a93-9ec8-a49e339d9e2c.png)


Then ssh to the server  
![image](https://user-images.githubusercontent.com/73797155/224580126-4bb9d215-bf41-412d-8e2b-46233d77a083.png)  

And run the bash script  
![image](https://user-images.githubusercontent.com/73797155/224580651-5d1bf242-1c61-4934-a954-e767db0bc48a.png)
![image](https://user-images.githubusercontent.com/73797155/224580666-40ff8d51-c5e4-43ca-851d-8247fd8a579d.png)





