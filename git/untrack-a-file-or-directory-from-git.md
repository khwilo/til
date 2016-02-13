# Untrack a directory from git

Normally this happens after you have already staged and committed the directory and its contents. The solution to untracking a file (removing it from the index), but still have it locally (in working tree) is:

```bash
$ git rm --cached <filename>
```

In the case of a directory you include the -r flag:

```bash 
$ git rm -r --cached <directory name>
```

*Then make a commit.*

**Remember to include the file or directory to the `.gitignore` of not already included.**

## Reference

[first_source](http://stackoverflow.com/questions/15027873/untrack-and-stop-tracking-files-in-git)
[second_source](http://stackoverflow.com/questions/22924633/gitignore-is-not-ignoring-directories)
