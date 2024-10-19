# CTF Report: Untangling Users Module

## Challenge 1: Becoming root with su
- **Flag:** `pwn.college{QkrsUuph1nwiO2UpURafeaRolay.dVTN0UDL3IjN1czW}`
- **Thought Process:** I used the `su` command to switch to the root user. After entering the password `hack-the-planet`, I read the `/flag` file.

---

## Challenge 2: Other Users with su
- **Flag:** `pwn.college{Mq1FKItD15j8307Jrs7GvTWF7Sg.dZTN0UDL3IjN1czW}`
- **Thought Process:** I used the `su` command with `zardus` as the user parameter. After entering the password `dont-hack-me`, I ran `/challenge/run` to get the flag.

---

## Challenge 3: Cracking Passwords
- **Flag:** `pwn.college{kf5MWlO2WZy5n6gldawYQUIV_-e.ddTN0UDL3IjN1czW}`
- **Thought Process:** I used the `john` command with the leaked password file to obtain the password for `zardus`. After finding the password `aardvark`, I used `su` to switch to `zardus`, then ran `/challenge/run` to retrieve the flag.

---

## Challenge 4: Using Sudo
- **Flag:** `pwn.college{IY7gGAGuI1bH0rkgjraaeOQ5sjB.dhTN0UDL3IjN1czW}`
- **Thought Process:** I used the `sudo` command to access root privileges and read the `/flag` file.
