# Overview

Points: 75
Category: General Skills

## Description

Someone's commits seems to be preventing the program from working. Who is it?

You can download the challenge files here:

[challenge.zip](https://artifacts.picoctf.net/c_titan/159/challenge.zip)

## Hints

In collaborative projects, many users can make many changes. How can you see the changes within one file?

Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).

You can use `python3 <file>.py` to try running the code, though you won't need to for this challenge.

## Approach

By typing `wget https://artifacts.picoctf.net/c_titan/159/challenge.zip` within the terminal we can download the challenge.zip file.

`unzip challenge.zip` and then `ls` we can see the directory `drop-in`

`cd drop-in` to enter the drop-in directory and then `ls` again to list all files which shows a `message.py` file

Trying to run the Python file with `python message.py` we get a syntax error, someone broke the code

Using `git log message.py`, we get the flag

```text
commit 23e9d4ce78b3cea725992a0ce6f5eea0bf0bcdd4
Author: picoCTF{@sk_th3_1nt3rn_81e716ff} <ops@picoctf.com>
Date:   Tue Mar 12 00:07:15 2024 +0000

    optimize file size of prod code
```

## Flag

picoCTF{@sk_th3_1nt3rn_81e716ff}
