# CTF Report: Pondering Paths Module

## Challenge 1: The root
- **Flag:** `pwn.college{UZo-oUEpeD4Qn2XwL7xjmxZEna1.dhzN5QDL3IjN1czW}`
- **Thought Process:** Executed the `pwn` command from its absolute path.
- **Command Used:** `/pwn`

---

## Challenge 2: Program and absolute paths
- **Flag:** `pwn.college{84QIGzVnnuU2E0ilj1LzCKq7z1h.dZDN1QDL3IjN1czW}`
- **Thought Process:** `run` is an executable program file that needs to be executed from its absolute path located under the challenge directory.
- **Command Used:** `/challenge/run`

---

## Challenge 3: Position thy self
- **Flag:** `pwn.college{YHnjbwN3TEdThT2ZPQO-XhSAkvI.ddDN1QDL3IjN1czW}`
- **Thought Process:** Executed `challenge/run`, which gave a different path (`/var/lib/apt/lists`). Changed the directory to `/var/lib/apt/lists` and executed `challenge/run` again.
- **Commands Used:** `cd /var/lib/apt/lists`, `./challenge/run`

---

## Challenge 4: Position else where
- **Flag:** `pwn.college{0TtVueXgdGvPvhpDnFQAGpGGwg8.dhDN1QDL3IjN1czW}`
- **Thought Process:** Executed `challenge/run` and was given a different path (`/usr/share/build-essential`). Changed the directory and executed `challenge/run`.
- **Commands Used:** `cd /usr/share/build-essential`, `./challenge/run`

---

## Challenge 5: Position yet elsewhere
- **Flag:** `pwn.college{skOf-l3iCP6Uv5Y993Kpqd9c1H_.dlDN1QDL3IjN1czW}`
- **Thought Process:** Executed `challenge/run` and was told to run it from the root directory.
- **Commands Used:** `cd /`, `/challenge/run`

---

## Challenge 6: Implicit relative paths, from /
- **Flag:** `pwn.college{wHKbCrIE7FelO7WxYLMEuykObAf.dBTN1QDL3IjN1czW}`
- **Thought Process:** Changed directory to root and executed `challenge/run` using an implicit relative path.
- **Commands Used:** `cd /`, `challenge/run`

---

## Challenge 7: Explicit relative paths from /
- **Flag:** `pwn.college{YFz7XVqf2K8CJT4wSnM8uxiW0-E.dFTN1QDL3IjN1czW}`
- **Thought Process:** Changed the working directory to root and used an explicit relative path to run the program `run`.
- **Commands Used:** `cd /`, `./challenge/run`

---

## Challenge 8: Implicit relative path
- **Flag:** `pwn.college{4Ih7TsKAA68oqbJmZCHEQVdxaNn.dlTM5QDL3IjN1czW}`
- **Thought Process:** Changed the working directory to `challenge` and ran the executable file `run` using a relative path.
- **Commands Used:** `cd challenge`, `./run`

---

## Challenge 9: Home sweet home
- **Flag:** `pwn.college{4e9xq_u-lRzsslJKk0TsvMZtfEC.dNzM4QDL3IjN1czW}`
- **Thought Process:** To pass an argument to the command `/challenge/run`, created a file `a` using `touch`, then used an absolute path with `~` (representing the home directory).
- **Commands Used:** `touch a`, `/challenge/run ~/a`
