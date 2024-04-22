# Overview

Points: 75
Category: General Skills

## Description

My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?

You can download the challenge files here:

[challenge.zip](https://artifacts.picoctf.net/c_titan/178/challenge.zip)

## Hints

`git branch -a` will let you see available branches

How can file 'diffs' be brought to the main branch? Don't forget to `git config`!

Merge conflicts can be tricky! Try a text editor like nano, emacs, or vim.

## Approach

By typing `wget https://artifacts.picoctf.net/c_titan/178/challenge.zip` within the terminal we can download the challenge.zip file.

`unzip challenge.zip` and then `ls` we can see the directory `drop-in`

`cd drop-in` to enter the drop-in directory and then `ls` again to list all files which shows a `flag.py` file

Using `cat flag.py` gives

```text
Printing the flag...
```

Checking `git branch -a` gives

```text
  feature/part-1
  feature/part-2
  feature/part-3
* main
```

Then `git checkout feature/part-1` to enter that branch

`cat flag.py` gives

```text
print("picoCTF{t3@mw0rk_", end='')
```

Then `git checkout feature/part-2` to enter that branch

`cat flag.py` gives

```text
print("m@k3s_th3_dr3@m_", end='')
```

Then `git checkout feature/part-3` to enter that branch

`cat flag.py` gives

```text
print("w0rk_6c06cec1}")
```

We can then combine all three parts to get the flag

## Flag

picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_6c06cec1}
