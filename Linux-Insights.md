# Learn Linux the Hard Way

## Data Manipulation

### Perusing Files
This occurs when you don't require to open a file editor to read the full length of the file. The command to use here will 
is called `less`. To view the contents of the zshrc file type:
 ```bash
 $ less .zshrc
 ```
 If you have a narrow window length you can read files horizontally by typing `--ch<ENTER><ENTER>`. This is after
 you have entered the `less` command. The command `-ch` is translated to `-chop-long-lines`. To search for an item type `/`
 followed by the name of the item to be searched.  
 `Less` allows one to scroll and search through streams of output that are too long for a single page. Another useful way in
 which it can be utilized is in printing information of running processes using `ps aux`.
 ```bash
 $ ps aux | less
 ```
 Piping the command with less enables one to scroll through the output easily. The arrow keys are useful in moving through the 
 output. To scroll forward a single page press the spacebar and to scroll backwards, press the key **b**.
