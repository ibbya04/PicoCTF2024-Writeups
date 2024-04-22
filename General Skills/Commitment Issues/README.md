# Overview

Points: 50
Category: General Skills

## Description

I accidentally wrote the flag down. Good thing I deleted it!
You download the challenge files here:

[challenge.zip](https://artifacts.picoctf.net/c_titan/76/challenge.zip)

## Hints

Version control can help you recover files if you change or lose them!

Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control)

You can 'checkout' commits to see the files inside them

## Approach

By typing `wget https://artifacts.picoctf.net/c_titan/76/challenge.zip` within the terminal we can download the challenge.zip file.

`unzip challenge.zip` and then `ls` we can see the directory `drop-in`

`cd drop-in` to enter the drop-in directory and then `ls` again to list all files which shows a `message.txt` file

With `cat message.txt`, we get

```text
TOP SECRET
```

As the hint suggested Git version control can help us recover lost files so I checked `git log`, which shows

```text
commit e720dc26a1a55405fbdf4d338d465335c439fb3e
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:10:06 2024 +0000

    create flag
```
With `git checkout e720dc26a1a55405fbdf4d338d465335c439fb3e` we can check out that commit

`ls` shows the same `message.txt` file but this time `cat message.txt` gives the flag

```text
picoCTF{s@n1t1z3_7246792d}
```

## Flag

picoCTF{s@n1t1z3_7246792d}
