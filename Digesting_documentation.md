# CTF Report: Digesting Documentation Module

## Challenge 1: Learning from Documentations
- **Flag:** `pwn.college{MctON8wnLOAi2vSr9wm3cLmk-51.dRjM5QDL3IjN1czW}`
- **Thought Process:** Initially tried to check the content of the current working directory (cwd) but was denied permission. Then I executed the command as specified in the challenge.
- **Command Used:** `/challenge/challenge –giveflag`

---

## Challenge 2: Learning Complex Usage
- **Flag:** `pwn.college{0Ws2G9klcEensu_MAjKGxmCPWy4.dVjM5QDL3IjN1czW}`
- **Thought Process:** Couldn’t understand the argument `printfile` at first. Investigated the directory contents and found that `not-the-flag` was a symbolic link to `flag`, so I used that as an argument to retrieve the flag.
- **Command Used:** `printfile not-the-flag`

---

## Challenge 3: Reading Manuals
- **Flag:** `pwn.college{k29cbgrpAho_82QxVhk_4T12Cvz.dRTM4QDL3IjN1czW}`
- **Thought Process:** Used the `man` command to understand the challenge and passed the necessary arguments to retrieve the flag.
- **Command Used:** `man challenge`, `<appropriate command from man>`

---

## Challenge 4: Searching Manuals
- **Flag:** `pwn.college{QgLloCxM2q7bE8W09fLba7hYG0E.dVTM4QDL3IjN1czW}`
- **Thought Process:** Used `/` to search within the manual for the correct argument to find the flag.
- **Command Used:** `man <program>`, `/flag`

---

## Challenge 5: Searching for Manuals
- **Flag:** `pwn.college{QSVGEUN9WvWoA9RLnnKtX69YQ8P.dZTM4QDL3IjN1czW}`
- **Thought Process:** Ran `man man` and tried the commands from the synopsis. Then `man`ned the alias of `/challenge/challenge` and used the command from there to retrieve the flag.
- **Command Used:** `man man`, `man challenge`, `<appropriate command>`

---

## Challenge 6: Helpful Programs
- **Flag:** `pwn.college{stMUNu-Rmexg4A7tfjqQ1kz66Cs.ddjM4QDL3IjN1czW}`
- **Thought Process:** Used the `help` command and passed the required arguments to complete the challenge and get the flag.
- **Command Used:** `help <command>`

---

## Challenge 7: Help for Builtins
- **Flag:** `pwn.college{wmPk7F_oa7H_4wdkAHsgZyi6G1a.dRTM5QDL3IjN1czW}`
- **Thought Process:** Used the `help` command on the built-in `challenge` command and passed the required arguments to retrieve the flag.
- **Command Used:** `help challenge`, `<appropriate arguments>`
