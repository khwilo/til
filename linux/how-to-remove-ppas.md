# HOW TO REMOVE PPAs IN LINUX  

## Method 1  
Use the **remove** flag:  
`sudo add-apt-repository --remove ppa:whatever/ppa`  

## Method 2  
Install **ppa-purge**: `sudo apt-get install ppa-purge`  
then remove the ppa: `sudo ppa-purge ppa_name`  

To also remove packages on the official repository do this: `sudo apt-get purge package_name`  

Source: [How can PPAs be removed?](http://askubuntu.com/questions/307/how-can-ppas-be-removed)
