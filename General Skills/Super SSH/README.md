# Overview

Points: 25
Category: General Skills

## Description

Using a Secure Shell (SSH) is going to be pretty important.
Can you `ssh` as `ctf-player` to `titan.picoctf.net` at port `52556` to get the flag?
You'll also need the password `1ad5be0d`. If asked, accept the fingerprint with `yes`.

## Hints

[SSH man page](https://linux.die.net/man/1/ssh)

You can try logging in 'as' someone with `<user>`@titan.picoctf.net

How could you specify the port?

Remember, passwords are hidden when typed into the shell

## Approach

Start by connecting to the server with `ssh ctf-player@titan.picoctf.net -p 52556`. Types `yes` to accept the fingerprint if asked and `1ad5be0d` as the password.

And straight away the flag is given!

`Welcome ctf-player, here's your flag...`

## Flag

picoCTF{s3cur3_c0nn3ct10n_8306c99d}
