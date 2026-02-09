# OverTheWireBanditGame

## OverTheWire: Bandit — My Notes

These are my personal notes and findings from completing the Bandit wargame.
I focused on identifying what each challenge teaches and the exact commands used.

---

## Level 1

List the files in the directory and read the readme file.

```bash
ls
cat readme
```

Password:
ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

---

## Level 2

The file is named -, so it must be accessed using a relative path.

```bash
cat ./-
```

Password:
263JGJPfgU6LtdEvgfWU1XP5yac29mFx

---

## Level 3

The file name contains spaces. Wrap it in quotes.

```bash
cat "spaces in this filename"
```

Password:
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

---

## Level 4

Use ls -a to view hidden files, then read .hidden.

```bash
ls -a
cat .hidden
```

Password:
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

---

## Level 5

Inspect file types to find the readable file.

```bash
file ./*
```

Then use cat on the correct file.

Password:
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

---

## Level 6

```bash
find */{.,}* | grep "ASCII text" | du -b -a | grep "1033"
```

I used the command above to find the password.  
I used `find */{.,}*` to view all the files including hidden files all together which `*` allowed for this.  
To use this command on the output of another command I used `|`.  
I used the `grep "ASCII text"` to only show the human readable files.  
I used the `du -b -a` to show me the byte size of all files.  
I used `grep "1033"` to only show files that have that byte size.  

At this point I already had the file I needed but you can add the command below to find the not executable file:

```bash
find ! -executable
```

Password:
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

---

## Level 7


```bash
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

I used `/` to search from the root directory.  
I used `-user`, `-group`, and `-size` to find the file based on information.  
The `c` represents bytes.  
`2>/dev/null` redirects the error messages to `/dev/null`, they are discarded making it easier to spot the actual matching file in the results.

Password:
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
