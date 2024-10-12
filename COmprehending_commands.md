# CTF Report: Comprehending Commands Module

## Challenge 1: cat not the pet but the command
- **Flag:** `pwn.college{g13Om11iM5dWMUDzptc_0GSVOwQ.dFzN1QDL3IjN1czW}`
- **Thought Process:** Used the `cat` command to read the `flag` file located in the home directory.
- **Command Used:** `cat flag`

---

## Challenge 2: catting absolute paths
- **Flag:** `pwn.college{4Ih7TsKAA68oqbJmZCHEQVdxaNn.dlTM5QDL3IjN1czW}`
- **Thought Process:** Used `cat` to read the `flag` file using its absolute path.
- **Command Used:** `cat /flag`

---

## Challenge 3: more catting practice
- **Flag:** `pwn.college{MljvjVca6TcaZRpMohC3XnTftZ-.dBjM5QDL3IjN1czW}`
- **Thought Process:** The `flag` file was in `/lib/python3.8/config-3.8-x86_64-linux-gnu/`. Used `cat` to read the file.
- **Command Used:** `cat /lib/python3.8/config-3.8-x86_64-linux-gnu/flag`

---

## Challenge 4: grepping for a needle in a haystack
- **Flag:** `pwn.college{kcdUaIfGp1S5XR_4UHedtkhNnEB.ddTM4QDL3IjN1czW}`
- **Thought Process:** The `flag` was in `challenge/data.txt`, a large file. Used `grep` with the argument `pwn`, since the flag always starts with "pwn".
- **Command Used:** `grep pwn challenge/data.txt`

---

## Challenge 5: listing files
- **Flag:** `pwn.college{IGGFUji4skO48iHkvk2Po94wLLz.dhjM4QDL3IjN1czW}`
- **Thought Process:** Used `ls` to list files in `/challenge`, found a renamed file `2465-renamed-run-21732` and executed it.
- **Command Used:** `ls /challenge`, `/challenge/2465-renamed-run-21732`

---

## Challenge 6: touching files
- **Flag:** `pwn.college{4Ih7TsKAA68oqbJmZCHEQVdxaNn.dlTM5QDL3IjN1czW}`
- **Thought Process:** Used the `touch` command to create files, changed directory to `/tmp`, and created files `college` and `pwn`, then executed `challenge/run`.
- **Command Used:** `cd /tmp`, `touch college`, `touch pwn`, `challenge/run`

---

## Challenge 7: removing files
- **Flag:** `pwn.college{c8CTR0XHUXB0mbZJoh3BMHijSU8.dZTOwUDL3IjN1czW}`
- **Thought Process:** Used the `rm` command to delete the `delete_me` file, then ran `challenge/check` to retrieve the flag.
- **Command Used:** `rm delete_me`

---

## Challenge 8: hidden files
- **Flag:** `pwn.college{sFTfBYmPrNBC2onFkNELecI_G1e.ddjN1QDL3IjN1czW}`
- **Thought Process:** Used `ls -a` to list hidden files, then used `cat` to read the hidden flag file.
- **Command Used:** `ls -a`, `cat .hiddenflag`

---

## Challenge 9: an epic filesystem quest
- **Flag:** `pwn.college{0uZersHrzwhB3YfLE4lasoKVTog.dljM4QDL3IjN1czW}`
- **Thought Process:** Changed directory to root, displayed hidden files, and read them using `cat`. Each hidden file provided a clue to the next directory. The clues led to directories in various locations:
  - EVIDENCE, .ALERT, TRACE-TRAPPED, .WHISPER, NOTE, CUE, TEASER, NUGGET.
  - Final directory: `/opt/ghidra/Ghidra/Processors/tricore/lib`.
- **Command Used:** Followed clues through different directories using `cat`.

---

## Challenge 10: making directories
- **Flag:** `pwn.college{0uZersHrzwhB3YfLE4lasoKVTog.dljM4QDL3IjN1czW}`
- **Thought Process:** Used `mkdir` to create `/tmp/pwd/` and used `touch` to create the file `college`. Then ran `/challenge/run`.
- **Command Used:** `mkdir /tmp/pwd/`, `touch college`

---

## Challenge 11: finding files
- **Flag:** `pwn.college{UJ0P0d088t8uNckOmsxV2aLnFXQ.dFzM4QDL3IjN1czW}`
- **Thought Process:** _(Not provided)_
- **Command Used:** _(Not provided)_

---

## Challenge 12: linking files
- **Flag:** `pwn.college{Qxgo5k1VifNoqvzJ6l1xPR5Fde8.dJzM4QDL3IjN1czW}`
- **Thought Process:** `/challenge/catflag` reads `~/not-the-flag`, but the real flag is in `/flag`. Created a symbolic link from `~/not-the-flag` to `/flag` and retrieved the flag by running `/challenge/catflag`.
- **Command Used:** `ln -s /flag not-the-flag`, `/challenge/catflag`
