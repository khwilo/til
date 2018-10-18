# UNSTAGE A FILE

- This situation normally arises when you stage file in git but later you want to unstage it.  
- The sequence of events may be:  
```bash
$ git add <filename>
```
- Then you consider to unstage it and stage another file instead or rather do something else. 
The git command **reset** is suitable for this situation and works as follows:  
```bash
$ git reset -- <filepath>
```

References:  
- This Stackoverflow question 
[Why are there 2 ways to unstage a file in git?](https://stackoverflow.com/questions/6919121/why-are-there-2-ways-to-unstage-a-file-in-git)
