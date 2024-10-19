# CTF Report: Perceiving Permissions Module

## Challenge 1: Changing File Ownership
- **Flag:** `pwn.college{8jsxEh9pSsJioSWSqlejiDUYoai.dFTM2QDL3IjN1czW}`
- **Thought Process:** I changed the ownership of `/flag` to `hacker` (my username) using the `chown` command and then read the file.

---

## Challenge 2: Groups and Files
- **Flag:** `pwn.college{wTRRq59zmhJ7-6VXaJ7vX44F_N6.dFzNyUDL3IjN1czW}`
- **Thought Process:** I changed the group ownership of `/flag` from `root` to `hacker` using `chown` and then read the file.

---

## Challenge 3: Fun with Group Names
- **Flag:** `pwn.college{Q7ZcyzgPYP6yCS10s41yuLKc1Qk.dJzNyUDL3IjN1czW}`
- **Thought Process:** I used the `id` command to find my group and changed the group of `/flag` to `grp15667` from `root` using `chown`, then read the file.

---

## Challenge 4: Changing Permissions
- **Flag:** `pwn.college{88ULh7Gi-nxahLKaA5ZC4qOo1t0.dNzNyUDL3IjN1czW}`
- **Thought Process:** To make `/flag` readable by users other than `root`, I used `chmod o+r` and then read the file.

---

## Challenge 5: Executable Files
- **Flag:** `pwn.college{A-PuRnwMLHTkvjKql5tluhExovn.dJTM2QDL3IjN1czW}`
- **Thought Process:** I inspected the file permissions with `ls -l` and found that only the `hacker` user and group could execute `/challenge/run`. I changed the group permission to executable using `chmod g+x`.

---

## Challenge 6: Permission Tweaking Practice
- **Flag:** `pwn.college{sTwLEwOiaslqIi5VHMB5sMiCZKu.dBTM2QDL3IjN1czW}`
- **Thought Process:** I followed a series of permission modifications as directed in the challenge, such as `chmod go-rwx`, `chmod go+wx`, and more. After completing the sequence, I was allowed to change the permissions of `/flag` to make it readable.

---

## Challenge 7: Permission Setting Practice
- **Flag:** `pwn.college{kQb2qzv21_E8lrpdhb-iCUhVNpm.dNTM5QDL3IjN1czW}`
- **Thought Process:** I executed a series of `chmod` commands with different user, group, and others permissions. After completing the tasks, I was allowed to use `chmod` on `/flag` to make it readable.

---

## Challenge 8: The SUID Bit
- **Flag:** `pwn.college{0klfPxAFS6VoRpywz8uEcI5MrIc.dNTM2QDL3IjN1czW}`
- **Thought Process:** I added the SUID bit to `/challenge/getroot` using `chmod`, which allowed me to access `/flag` and read the file.
