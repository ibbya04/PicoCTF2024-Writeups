# Overview

Points: 50
Category: General Skills

## Description

What was I last working on? I remember writing a note to help me remember...

You can download the challenge files here:

[challenge.zip](https://artifacts.picoctf.net/c_titan/162/challenge.zip)

## Hints

The `cat` command will let you read a file, but that won't help you here!

Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).

When committing a file with git, a message can (and should) be included.

## Approach

By typing `wget https://artifacts.picoctf.net/c_titan/162/challenge.zip` within the terminal we can download the challenge.zip file.

`unzip challenge.zip` and then `ls` we can see the directory `drop-in`

`cd drop-in` to enter the drop-in directory and then `ls` again to list all files which shows a `message.txt` file

With `cat message.txt`, we get

```text
This is what I was working on, but I'd need to look at my commit history to know why...
```

`git log`, shows

```text
commit 712314f105348e295f8cadd7d7dc4e9fa871e9a2 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:26 2024 +0000

    picoCTF{t1m3m@ch1n3_e8c98b3a}
```

## Flag

picoCTF{t1m3m@ch1n3_e8c98b3a}
