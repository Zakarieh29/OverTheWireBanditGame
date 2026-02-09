# OverTheWireBanditGame
OverTheWire: Bandit — My Notes

These are my personal notes and findings from completing the Bandit wargame.
I focused on identifying what each challenge teaches and the exact commands used.

Level 1
List the files in the directory and read the readme file.

ls
cat readme
Password: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

Level 2
The file is named -, so it must be accessed using a relative path.

./-
Password: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx

Level 3
The file name contains spaces. Wrap it in quotes.

cat "spaces in this filename"
Password: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

Level 4
Use ls -a to view hidden files, then read .hidden.

ls -a
cat .hidden
Password: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

Level 5
Inspect file types to find the readable file.

file ./*
Then use cat on the correct file.

Password: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

Level 6
Search for a regular file with a specific size.

find . -type f -size 1033c
Then read the file.

Password: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

Level 7
