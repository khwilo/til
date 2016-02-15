Sometimes one ends up writing a wrong thing in a commit message. The below steps solves the problem:  

```
git commit --amend
```

This opens your editor, allowing you to change the commit message of the recent commit.  

You can also set the commit message directly from the command line:  

```
git commit --amend -m "New commit message"
```

## NOTE
Always counter check your message before commiting.  

## REFERENCE
[link](http://stackoverflow.com/questions/179123/edit-an-incorrect-commit-message-in-git)
