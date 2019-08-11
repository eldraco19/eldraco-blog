+++
title = "The GNU Stream editor - sed"
date = "2019-06-20"
author = "Ayush Karn"
tags = ['Linux','sed']
+++


`sed` is a stream editing tool made by GNU. A stream editor is used to perform
text transformations on a input stream ( a file or redirected input from a pipe ).
sed works by taking an edit script and modifies the input stream according to the edit
script.

`sed` comes pre-installed in most of the linux and unix based distributions and can also
be installed easily from the distribution's package manager.

A basic sed invocation can be :

```bash
sed SCRIPT INPUTFILE...
```

Now let's look at the following file **INPUT.txt** ..

![](/../../screen1.png)

now if you want to change all the occurences of 'Linux' to 'Windows' , you can simply do this :

```bash
sed 's/Linux/Windows/' INPUT.txt
```

the output will be

![](/../../screen2.png)

here 's' stands for substitution followed by the string/pattern to be replaced and the replacement string.

It's easy , isn't it ?

**sed** also takes regular expressions as input , which can come handy in times.

Some common regular expresssion are :

**.\*** - matches multiple string of any length.

**^a** - matches all the lines starting with a.

**a.** - matches a single character after a .

**xyz\$** - matches all the lines ending with xyz.

**p[io]ng** - matches ping and pong.

**p[a-z]ng** - middle character can be anything from a to z.

**p[A-Z]ng** - middle character can be anything from A to Z.

**p[^a]ng** - middle character can be anything except a.

Now for this file ..
<br><br>
![INPUT FILE](/../../screen3.png)

<br><br>
![INPUT FILE](/../../screen4.png)

<br><br>

Now by now you must have noticed that the output is always to the stdout , but what if
we want the do the change in the file itself ?

This can be done with a _i_ flag ,
<br><br>
![INPUT FILE](/../../screen5.png)

<br><br>

and if we want the output to be in a different file then ,  
<br><br>
![INPUT FILE](/../../screen6.png)

<br><br>
