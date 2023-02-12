## Lab Report 3

For this lab report I will be talking about the `find` command.  
`find` is is a very useful command that can be used to find files by  
several different criteria, depending on which options you use.  
The command takes the general form  
`$ find [where to start searching from] [expression determines what to find] [-options] [what to find]`


One very useful option for this command is `-name` which allows you to search for files by the name.
For instance, if you wanted to search for all the `.txt` files in a folder, you would use this  
```gitbash
$ find written_2/ -name "*.txt"
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
written_2/non-fiction/OUP/Abernathy/ch15.txt
.
.
.
written_2/travel_guides/berlitz2/Vallarta-History.txt
written_2/travel_guides/berlitz2/Vallarta-WhatToDo.txt
written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt
```
This command searches through written_2 and all of its subdirectories and prints all the files that end with `.txt`. 
This is useful if you want to count the number of files in a directory of a certain type or pattern.  
  
  
You can also use this option to search for the names of the files. For instance, if you wanted to search for `"China"`
```gitbash
$ find written_2/ -name "China*"
written_2/travel_guides/berlitz2/China-History.txt
written_2/travel_guides/berlitz2/China-WhatToDo.txt 
written_2/travel_guides/berlitz2/China-WhereToGo.txt
```
This is helpful when you know the name of the file, but don't know the path. You can use the find command to find the desired files.  

Another option is `-path` which allows you to find files based on the path you give it
```gitbash
$ find written_2/ -path "*/Abernathy/*"
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
written_2/non-fiction/OUP/Abernathy/ch15.txt
written_2/non-fiction/OUP/Abernathy/ch2.txt
written_2/non-fiction/OUP/Abernathy/ch3.txt
written_2/non-fiction/OUP/Abernathy/ch6.txt
written_2/non-fiction/OUP/Abernathy/ch7.txt
written_2/non-fiction/OUP/Abernathy/ch8.txt
written_2/non-fiction/OUP/Abernathy/ch9.txt
```
This is useful if you want to find all the files in a directory, or you know the path without knowing the name.  

```
$ find written_2/ -path "*/berlitz2/Vallarta*"
written_2/travel_guides/berlitz2/Vallarta-History.txt
written_2/travel_guides/berlitz2/Vallarta-WhatToDo.txt
written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt
```
If you know the folder of the file your looking for, it may be faster to use this command rather than the `-name` option.  

Another option is to use the `-size n` command to search for files as large or larger than n bytes. You can use multiple suffixes for different sizes.
`c` is 1 byte
`w` is 2 bytes
`k` is a kibibyte (1024 bytes)
`M` is for mibibyte (1024x1024 bytes)
The values of the files are rounded up to the nearest unit of choice.
```
$ find written_2/ -size 20k
written_2/non-fiction/OUP/Castro/chV.txt
written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt
written_2/travel_guides/berlitz2/Poland-History.txt
written_2/travel_guides/berlitz2/Poland-WhatToDo.txt
```
If you wanted to find a file thats over 20 kibibytes you would use the above command. 
This is useful if you want to find the largest files in a folder.  

You can also use this command to find files smaller than a certain size.
```
$ find written_2/ -name "*.txt" -size -3k
written_2/travel_guides/berlitz1/HandRHongKong.txt
written_2/travel_guides/berlitz1/HandRIbiza.txt
written_2/travel_guides/berlitz1/HandRIstanbul.txt
written_2/travel_guides/berlitz1/HandRJerusalem.txt
written_2/travel_guides/berlitz1/HandRLakeDistrict.txt
written_2/travel_guides/berlitz1/HandRLasVegas.txt
written_2/travel_guides/berlitz1/HandRLisbon.txt
written_2/travel_guides/berlitz1/HandRLosAngeles.txt
written_2/travel_guides/berlitz1/HandRMadeira.txt
written_2/travel_guides/berlitz1/HandRMallorca.txt
```
Now it finds the `.txt` files that are smaller than 3 kibibytes, which would be useful if you wanted to find the shortest files.  

You can also search for file by the type. If you wanted a list of directories, you could use the `-type` option.

```
$ find written_2/ -type d
written_2/
written_2/non-fiction
written_2/non-fiction/OUP
written_2/non-fiction/OUP/Abernathy
written_2/non-fiction/OUP/Berk
written_2/non-fiction/OUP/Castro
written_2/non-fiction/OUP/Fletcher
written_2/non-fiction/OUP/Kauffman
written_2/non-fiction/OUP/Rybczynski
written_2/travel_guides
written_2/travel_guides/berlitz1
written_2/travel_guides/berlitz2
```
If you wanted to search for the directories, you could use `-type d` which would print all the different directories in the specified folder. 
This allows you to get a good idea of what the file system looks like.  

```
$ find written_2/ -type f
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
written_2/non-fiction/OUP/Abernathy/ch15.txt
.
.
.
written_2/travel_guides/berlitz2/Vallarta-History.txt
written_2/travel_guides/berlitz2/Vallarta-WhatToDo.txt
written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt
```
You could also use `-type f` to search for all the regular files in the specified folder. 
Since there are only `.txt` files in this directory, it has the same effect as searching `-name "*.txt*` allowing you see and count every file in the directory.
