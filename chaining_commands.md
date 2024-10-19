# CTF Report: Chaining Commands Module

## Challenge 1: Chaining with Semicolons
- **Flag:** `pwn.college{QZIHIJXwliWllE4QnBi_kSNOzGL.dVTN4QDL3IjN1czW}`
- **Thought Process:** Executed `/challenge/pwn` followed by `/challenge/college` using a semicolon to chain the commands.

---

## Challenge 2: Your First Shell Script
- **Flag:** `pwn.college{ct4NSqiLqV2fUs7MqcAa3ruwRWV.dFzN4QDL3IjN1czW}
`
- **Thought Process:** 

---

## Challenge 3: Redirecting Script Output
- **Flag:** `pwn.college{wH0baQnFJVPnB5LVLXt-gz5EK2-.dhTM5QDL3IjN1czW}`
- **Thought Process:** Created a bash file `x.sh` using `touch`. Then used the `echo` command with the required chained commands in quotes and redirected the output to `x.sh`.

---

## Challenge 4: Executable Shell Scripts
- **Flag:** `pwn.college{QCDNYUDHe9LSdGwvdSQe5U0myRr.dRzNyUDL3IjN1czW}`
- **Thought Process:** Created a bash file `x.sh` using `touch`. Used the `echo` command with the required chained commands in quotes and redirected the output to `x.sh`. Modified the file permissions using `chmod` to make it executable, and ran `./x.sh` to retrieve the flag.
