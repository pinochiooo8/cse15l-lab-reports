# Lab Report 1

1.  using the `cd` command with no arguments.
    The working directory was `/home` when the command was run. I don't get any output because the `cd` command successfully runs, no arguments means that the `cd` command will take me back to the `home` directory. The output is not an error.
   
```
[user@sahara ~]$ cd
[user@sahara ~]$ pwd
/home
```
2.   using the `cd` command with a path to a directory as an argument.
    The working directory was `/home/lecture1` when the command was run. I don't get any output because the `cd` command successfully runs, it changes the working directory from
   `/home` to `/home/lecture1`. The output is not an error. 
   
```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ pwd
/home/lecture1
```

3. using the `cd` command with a path to a file as an argument.
   The working directory was `/lecture1/messages` when the command was run. I get the message Not a directory because the cd command can only be used on a directory, not a file. The output is not an error, because it is supposed to generate an error message since the `cd` command doesn't support the file as an argument. 

```
[user@sahara ~]$ cd lecture 1
[user@sahara ~/lecture1]$ cd messages
[user@sahara ~/lecture1/messages]$ cd en-us.txt
bash : cd : en-us.txt : Not a directory
```

4.  using the `ls` command with no arguments.
    The working directory was `/home` when the command was run. It will generate a list of files and directories from the current working directory, so there is `'Lab 1'  lecture1 new1 'newlecture' `in the `home` directory. The output is not an error.

```
[user@sahara ~]$ ls
'Lab 1'  lecture1 new1 'newlecture'
```

5.  using the `ls` command with a path to a directory as an argument.
     The working directory was `/home` when the command was run. It will generate a list of files and directories, in this case(Hello.class Hello.java messages README) from the directory `lecture1` which I put as an argument. The output is not an error. 

```
[user@sahara ~]$ ls lecture1
Hello.class Hello.java messages README
```

6.  using the `ls` command with a path to a file as an argument.
     The working directory was `/home/lecture1/messages` when the command was run. Instead of generating a list, when we using the file as an argument, the `ls` command will check the existence of the file name in that specific directory. In this case, there does exist a file name `en-us.txt` in the `/lecture1/messages` directory. The output is not an error. 
```
[user@sahara ~]$ cd lecture 1
[user@sahara ~/lecture1]$ cd messages
[user@sahara ~/lecture1/messages]$ ls en-us.txt
en-us.txt
```

7.  using the `cat` command with no arguments.
    The working directory was `/home` when the command was run. For the output, when I hit enter after the `cat` command, it waited for my input, so I typed in 'test', as a result, the system returned the `'test'` to me and ended. The output is not an error. 

```
[user@sahara ~]$ cat
test
test
```

8.  using the `cat` command with a path to a directory as an argument.
    The working directory was `/home` when the command was run. For the output, it seems that the `cat` command only accepts file or blank as an argument, it does not support directory as an argument. The output is not an error. 
    
```
[user@sahara ~]$ cat lecture1
cat: lecture1 : Is a directory
```

9.   using the `cat` command with a path to a file as an argument.
    The working directory was `/lecture1/messages` when the command was run. For the output, it prints out the content of the file `en-us.txt`, Hello World!. The output is not an error. 
 ```
[user@sahara ~]$ cd lecture 1
[user@sahara ~/lecture1]$ cd messages
[user@sahara ~/lecture1/messages]$ cat en-us.txt
Hello World!
```
    



