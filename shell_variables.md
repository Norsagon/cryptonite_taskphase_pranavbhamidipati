# CTF Report: Shell Variables Module

## Challenge 1: Printing Variables
- **Flag:** `pwn.college{EsVkrXRDMydFygcUacF3NoS_dZB.ddTN1QDL3IjN1czW}`
- **Thought Process:** I passed the variable `FLAG` as an argument to `echo`, prepending it with a `$` sign to print its value.

---

## Challenge 2: Setting Variables
- **Flag:** `pwn.college{0IYYIensJzmFL6mm725bkNf9pLI.dlTN1QDL3IjN1czW}`
- **Thought Process:** I assigned the value `PWN` to the variable `COLLEGE` using `=`.

---

## Challenge 3: Multi-Word Variables
- **Flag:** `pwn.college{4T1qh4NM1MWaynwOorgbmRemFAQ.dBjN1QDL3IjN1czW}`
- **Thought Process:** I assigned the value `PWN` to two words as a single token using quotes.

---

## Challenge 4: Exporting Variables
- **Flag:** `pwn.college{UnuGnaTrCoYR8k9wdkGBADSefJl.dJjN1QDL3IjN1czW}`
- **Thought Process:** I exported the variable `COLLEGE` and assigned it the value `PWN`, then assigned `pwn` to `college` without using `export`.

---

## Challenge 5: Printing Exported Variables
- **Flag:** `pwn.college{kfmvzvuZwi3QdAuFHld4RTqMLIi.dhTN1QDL3IjN1czW}`
- **Thought Process:** I used the `env` command to print all the environment variables and their corresponding values.

---

## Challenge 6: Storing Command Outputs
- **Flag:** `pwn.college{kPemWlOWyUA70ClQZEEoMFDaMjM.dVzN0UDL3IjN1czW}`
- **Thought Process:** PWN=$(/challenge/run) and then ran echo $PWN to get the flag.
---

## Challenge 7: Reading Input
- **Flag:** `pwn.college{gwPirqWrHvYfKGsg_lVmcfPrV2b.dhzN1QDL3IjN1czW}`
- **Thought Process:** I used `read -p` to take input from the user as “me” and stored it in the variable `PWN`. The input was `COLLEGE` and was printed out using `echo`.

---

## Challenge 8: Reading Files
- **Flag:** `pwn.college{wD8FLitE281NBTxYbmfrMOi-mpt.dBjM4QDL3IjN1czW}`
- **Thought Process:** I directed the output of `/challenge/read_me` to be the input for the `read` command into the variable `PWN`.
