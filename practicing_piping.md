# CTF Report: Practicing Piping Module

## Challenge 1: Redirecting Output
- **Flag:** `pwn.college{Q-dFQAmaHj4C5EluNy5S6UoZPN_.dRjN1QDL3IjN1czW}`
- **Thought Process:** As instructed, I used the query to redirect my output from `echo` to the file `college`.
- **Command Used:** `echo <data> > college`

---

## Challenge 2: Redirecting More Output
- **Flag:** `pwn.college{ceZRytB4dOTzCl2PlXEd5XgRFx3.dVjN1QDL3IjN1czW}`
- **Thought Process:** I directed the command `/challenge/run` to `myfile` and read its contents using `cat`.
- **Command Used:** `/challenge/run > myfile`, `cat myfile`

---

## Challenge 3: Appending Output
- **Flag:** `pwn.college{Ylnk-HX1rtROVkJO8l3PaZR3ncX.ddDM5QDL3IjN1czW}`
- **Thought Process:** I appended the output using `>>` and read the contents with `cat`, which gave me the flag.
- **Command Used:** `echo <data> >> myfile`, `cat myfile`

---

## Challenge 4: Redirecting Errors
- **Flag:** `pwn.college{sFTfBYmPrNBC2onFkNELecI_G1e.ddjN1QDL3IjN1czW}`
- **Thought Process:** I understood how to work with different streams and directed standard output to `myfile` and errors to `instructions`.
- **Command Used:** `<command> 1>myfile 2>instructions`

---

## Challenge 5: Redirecting Input
- **Flag:** `pwn.college{0eRZo9iyXcdBMkpxG118BmZrmF2.dBzN1QDL3IjN1czW}`
- **Thought Process:** I channeled the output to `pwn` and took `pwn`'s input for `/challenge/run`.
- **Command Used:** `cat pwn | /challenge/run`

---

## Challenge 6: Grepping Stored Results
- **Flag:** `pwn.college{ka3Tgt-mZTEn_Zn0Ptcvl0fk-Pc.dhTM4QDL3IjN1czW}`
- **Thought Process:** I redirected the output to a file and used `pwn` as the parameter for the `grep` command.
- **Command Used:** `<command> > result.txt`, `grep pwn result.txt`

---

## Challenge 7: Grepping Live Output
- **Flag:** `pwn.college{0XPztVjpcoDypTQvHYXrvpa9KP8.dlTM4QDL3IjN1czW}`
- **Thought Process:** Executed `/challenge/run` and piped the output as input to `grep`, using `pwn` as the parameter to capture the flag.
- **Command Used:** `/challenge/run | grep pwn`

---

## Challenge 8: Grepping Errors
- **Flag:** `pwn.college{Yg-9RETVFZv6-us1m728Q08Uo9a.dVDM5QDL3IjN1czW}`
- **Thought Process:** I executed `/challenge/run` and redirected the error output using `2>&1`, then piped it to `grep` with `pwn` as the argument.
- **Command Used:** `/challenge/run 2>&1 | grep pwn`

---

## Challenge 9: Duplicating Piped Data with `tee`
- **Flag:** `pwn.college{M1Twp3EP01HV7ia61WFiS0zr4Q0.dFjM5QDL3IjN1czW}`
- **Thought Process:** Piped the data to two files using `tee`. First, I used `cat` to display error information, then I executed the reformed code.
- **Command Used:** `<command> | tee file1 file2`, `cat file1`, `<command>`

---

## Challenge 10: Writing to Multiple Programs
- **Flag:** `pwn.college{0Qfl-d61C9eeexjz5M9rYTU61-J.dBDO0UDL3IjN1czW}`
- **Thought Process:** (Fill in your thought process here)
- **Command Used:** (Fill in your command here)

---

## Challenge 11: Split Piping `stderr` and `stdout`
- **Flag:** `pwn.college{AZXrhPbld7X-8I5eNzB9y1leo_q.dFDNwYDL3IjN1czW}`
- **Thought Process:** (Fill in your thought process here)
- **Command Used:** (Fill in your command here)
