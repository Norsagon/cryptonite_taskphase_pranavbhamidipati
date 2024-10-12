# CTF Report: /file globbing Module

## Challenge 1: Matching with *
- **Flag:** `pwn.college{gSKr6U7vGDZ16Yjund6VhhB14b1.dFjM4QDL3IjN1czW}`
- **Thought Process:** Used the `*` wildcard to match any string of characters, including no characters, in filenames.

---

## Challenge 2: Matching with ?
- **Flag:** `pwn.college{odsvnvPiVexS04m306Mg4hOWPXa.dJjM4QDL3IjN1czW}`
- **Thought Process:** Used the `?` wildcard to match exactly one character in the filename.

---

## Challenge 3: Matching with []
- **Flag:** `pwn.college{MIUbQ6aohdYMq9mzz1Ps7V4ALH_.dNjM4QDL3IjN1czW}`
- **Thought Process:** Used `[]` to specify a set of characters that can match in filenames, e.g., `[a-z]` for any lowercase letter.


---

## Challenge 4: Matching paths with []
- **Flag:** `pwn.college{kcW01kldDBmz6DzuV83y5qt5kGa.dRjM4QDL3IjN1czW}`
- **Thought Process:** Used square brackets `[]` to match specific paths, where only certain characters or ranges are valid.

---

## Challenge 5: Mixing globs
- **Flag:** `pwn.college{8E97Tvg2NQhHzNCicvU8E0kIcZj.dVjM4QDL3IjN1czW}`
- **Thought Process:** Combined multiple glob patterns to [cep]* to uniquely identify files or paths where the first character was distinct.[] finds the files which have the first letter as specified and * expands it
---

## Challenge 6: Exclusionary globbing
- **Flag:** `pwn.college{gAwKUh5MURytkngtO1ygBoVSYrr.dZjM4QDL3IjN1czW}`
- **Thought Process:** Used exclusionary globbing with `[!pwn]*` to exclude files or paths starting with `pwn`, while using `*` to match the rest.
