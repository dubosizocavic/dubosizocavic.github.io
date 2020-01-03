---
layout: default
---

## General info

This is the content of my Command line course, as I remember it now.

## Week 1
The first week of our course was mostly about understanding what command line is and **setting up** our comupter in order to be able to practice for the course. We also learnt some basic commands. We learnt:  
* how to navigate through directories,
* how to manipulate files (open, copy, remove, edit),
* how to manipulate directories (open, copy, remove),
* to distinguish what's the difference when the same command is applied on files and directories,
* to add options after commands.

Most of commands were very simple and consisted of only one string of characters: **less**, **rm**, **whoami** etc.

How command **rm** works for single and multiple files:  
```shell
$ rm file1.txt
```
This command will remove file1.txt.
```shell
$ rm file1.txt file2.txt
```
This command will remove file1.txt and file2.txt.

## Week 2
In the second week we learnt how to connect to a **remote server**. This is when I started feeling like a level pro. We also leant **running proccesses in the background**, **killing proccesses** using their PID. We learnt how to find the root folder of our computer and went thought its content.  
Already in the second week I started solving problems by myself. My problem was that my username in CSC was different from my username on the computer, so I had to find a solution to that and it was that we must specify our username on the server:
```shell
$ ssh \<username\>@\<servername\>
```

## Week 3
In the third week we learnt how to use many useful commands to **process a text**. Many of them are going to be useful for my other project related to easy-to-read Finnish.

| COMMAND | DESCRIPTION                                               | LEARNT |
|---------|:---------------------------------------------------------:|-------:|
| sort    | command which prints lines of a file in a sorted order    | yes    |
| uniq    | command which filters out repeated lines in a text file   | yes    |
| tr      | command which transforms (inclusing deleteing) characters | yes    |
| egrep   | command which searches for patterns of characters         | yes    |

Example:
```
$ sort list_of_words.txt
```

This command will return the list of words in the alphabetical order.


## Week 4
The forth week was about writing complex **command pipelines** and getting an output file after performing all of them together. The most important command of that week was **sed**. It works similar to egrep in sense that it is looking for some patterns, but it also has an option of substituting those patterns with some other patterns.  
This week was time-consuming for me, so I didn't manage to complete the quiz because I ran out of time even though I stated working on it three days before the deadline. This is when I felt that the workload on the course goes beyond 5 ECTS and that there was too much new information in the tasks.  
Example:
```
$ cat katinka_rabe.utf8.txt | egrep "ssa\b"
```
This command will open the text katinka_rabe.utf8.txt and select all the strings of characters ending in ssa.


## Week 5
This week was the most demanding for me. It was about writing **scripts**. I felt that I understood all of the instructions, but when I procceeded to the quiz, I could not solve some problems and I thought that the requirements are too high for what we are taught in the instructions. I understood how to turn a command pipeline into a script, but the tasks given were a completely new level. I also learnt the basics of the **if statement**. I learnt about **environment variables** and how to change/use them. I also got to know how to **personalize my working environment**.
Example:
```
diff $1 $2 > /dev/null
if [ $? -eq 0 ]
then
    echo "0"
else
    echo "1"
fi
```
This is part of the script which is suppose to compare two files and echo 0 id they are the same or echo 1 if they are different.

## Week 6
In the 6th week I started feeling like I was doing some real programming. We learnt how to **install software**, how to solve a problem if software could not be installed. We also installed **python packages** and use **python interpreter**. I liked what **Makefile** does and it was fun to do the exercizes with it.
Example:
```Makefile
merge:
        cat data/*no_md.txt > data/all.no_md.txt
```
This is part of my Makefile file, which is supposed to merge all files ending in "no_md.txt".  

## Week 7
In the 7th week we got acquainted with the concept of **version control**, which is very useful for experimenting with out own or somebody else´s code. We installed git and made a **GitHub account**. I had no idea that GitHub functions like that and I was impressed with the magic. On the other hand, it is a bit scary that someone can read everything I did there. However, no one is probably interested, except the teachers reading at the end of the course. The concept of **branches** is a bit abstract, but I understand how it works.
```
$ git branch dusica
$ git checkout dusica
```
The first command will create the new branch "dusica" and the second command will switch to that branch.

Finally, in the final assignment we learnt about **GitHub pages**. They are used for creating our own website based on the repository on GitHub. It is done with a help of **Jekyll**, which is a site generator. Jekyll helps us preview what we have built on our webpage. We don't need to push our changes to GitHub every time we make them, we can use Jekyll to preview what we have made and push the changes if we like the result.  
My home page in the end looks like this:  

![screenshot](webpage_pic.png.PNG)