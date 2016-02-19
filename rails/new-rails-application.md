# New Rails Application  

This is how you create a project-specific gemset, installing Rails, and creating a new application.  
```bash
$ mkdir myapp
$ cd myapp
$ rvm use ruby-2.3.0@myapp --ruby-version --create
$ gem install rails
$ rails new .
```  

The application is named "myapp". Creating a project-specific gemset is on line 3 where the option `--ruby-version` creates **.ruby-version** and **.ruby-gemset** files in the root directory. RVM loads the required version of Ruby and the correct gemset whenever you enter the directory.  
When creating the gemset, it will be empty, thus we install Rails using the following command `gem install rails`. It installs the most recent release of Rails.  
Running `rails new .` uses the Unix "dot" convention to refer to the current directory. This assigns the name of the directory to the new application. 
