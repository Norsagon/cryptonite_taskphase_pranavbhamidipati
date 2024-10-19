# CTF Report: Processes and Jobs Module

## Challenge 1: Listing Processes
- **Flag:** `pwn.college{00arRdP95Fh0uU5MRof95VBVUdU.dhzM4QDL3IjN1czW}`
- **Thought Process:** I listed the running processes and found a renamed `/challenge/run` command running as `/challenge/12045-run-7751`.

---

## Challenge 2: Killing Processes
- **Flag:** `pwn.college{0-N-TZmHgNtaENylb2_pPOTap-k.dJDN4QDL3IjN1czW}`
- **Thought Process:** I listed the running processes and killed the process with the name `don't run` using its process ID.

---

## Challenge 3: Interrupting Processes
- **Flag:** `pwn.college{Q-GCiZgWJCSEAmrOUezPES4NZCs.dNDN4QDL3IjN1czW}`
- **Thought Process:** I ran the `/challenge/run` command and interrupted it using `Ctrl+C` to get the flag.

---

## Challenge 4: Suspending Processes
- **Flag:** `pwn.college{ccMfMb6UZQMbWlUI4VBVMZzngEn.dVDN4QDL3IjN1czW}`
- **Thought Process:** I executed `/challenge/run`, suspended the process using `Ctrl+Z`, and then executed another `/challenge/run` to get the flag.

---

## Challenge 5: Resuming Processes
- **Flag:** `pwn.college{MDrUpKXtMrMZJl6y3UPQUGlApOJ.dZDN4QDL3IjN1czW}`
- **Thought Process:** After suspending `/challenge/run` with `Ctrl+Z`, I resumed it using the `fg` command to get the flag.

---

## Challenge 6: Backgrounding Processes
- **Flag:** `pwn.college{gTLTT-5IdNVk2oCE6Ru6uNOHIpW.ddDN4QDL3IjN1czW}`
- **Thought Process:** I suspended the process with `Ctrl+Z`, resumed it in the background using `bg`, and then executed another `/challenge/run` to get the flag.

---

## Challenge 7: Foregrounding Processes
- **Flag:** `pwn.college{QtHyqUeZWZi5syi2tm9vj2pua6M.dhDN4QDL3IjN1czW}`
- **Thought Process:** I suspended the process using `Ctrl+Z`, resumed it in the background with `bg`, and then brought it back to the foreground using `fg`.

---

## Challenge 8: Starting Backgrounded Processes
- **Flag:** `pwn.college{w1bVSTMjwNKKqsqco8N_nm9y1au.dlDN4QDL3IjN1czW}`
- **Thought Process:** I ran the process in the background directly using an `&` at the end.

---

## Challenge 9: Process Exit Codes
- **Flag:** `pwn.college{AaU-q9O9JeCLh6NVIcwoSFFD-RH.dljN4UDL3IjN1czW}`
- **Thought Process:** I executed `/challenge/get-code`, printed the exit code using `$?`, and then used the exit code as the argument for `/challenge/submit-code`.
