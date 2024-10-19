# CTF Report: Pondering Path Module

## Challenge 1: The PATH Variable
- **Flag:** `pwn.college{Ia0TUHi_njA0XIi4KKAnrK1akNY.dZzNwUDL3IjN1czW}`
- **Thought Process:** Rewrote the `PATH` to only include `/run/challenge/bin`. Executed `challenge/run` to retrieve the flag.

---

## Challenge 2: Setting PATH
- **Flag:** `pwn.college{svqqy95hfAx8C7tUNVGdjRpi8Oj.dVzNyUDL3IjN1czW}`
- **Thought Process:** Updated the `PATH` to include `more_commands`. Ran `challenge/run` to get the flag.

---

## Challenge 3: Adding Commands
- **Flag:** `pwn.college{Ulaye7lIK-mnzisCZk8vlczsTzp.dZzNyUDL3IjN1czW}`

- **Thought Process:** 
-*Thought Process:*  we create a file win using touch command then use echo and the > symbol to write the 'cat /flag' command into the win file, then use chmod to add executeable permissions for the win file, copy the original path variable contents and then modify it to add the home path to it, without rewriting, this removes the problem of not being able to use cat command (this was done because the read command was giving an invalid identifier error) then use /challenge/run to get the flag .
---

## Challenge 4: Hijacking Commands
- **Flag:** `pwn.college{E2e7Xd1Vg3z79QYiY4jF3cQBBAi.ddzNyUDL3IjN1czW}`
- **Thought Process:** Created a file named `rm` in my home directory using `touch`. Used `echo` to write `cat /flag` into the `rm` file. Made the file executable with `chmod`, added `/home/hacker` to the beginning of the `PATH`, and then executed `run` to complete the challenge.
















---
