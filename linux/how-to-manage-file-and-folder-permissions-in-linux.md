# How to manage file and folder permissions in linux

## Command line: File permissions

The commands for modifying file permissions and ownership are:

```
chmod - change permissions
chown - change ownership
```
*NOTE :* The only user that can modify the permissions or ownership of a file is either the current user or the root user.  

### Demonstration

If you want different users to have read and write access to a particular folder then make them join a special group. If you know the users in your system and know your network is safe then change the permissions of the folder to give them access:  

`sudo chmod -R ugo+rw /path/to/file`  

The breakdown of the above command:  

```
sudo   - gain admin rights for the command
chmod  - the command to modify permissions
-R     - modifies permission of the parent folder and the child objects within (recursive)
ugo+rw - give User, Group and Other read and write access
```

The `other` entry effectively gives everyone permission to the folder / file.  

The permissions you can give to a file or a folder are:  

```
r - read
w - write
x - execute
```

## Command line: File ownership
Lets say you have Khwilo moved a folder for Noel into the SHARE directory- but Khwilo still has ownership. This can be done with a simple command:  

`sudo chown -R noel /path/to/file`  

Breaking the above command down:  

```
sudo  - gain admin rights for the command
chown - command for changing ownership
-R    - the recursive switch to make sure all child objects get the same ownership changes
noel   - the new owner of the folder
```
