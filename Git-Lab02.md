### This is continue to the previous Lab, Login to EC2 instance


#### Create a directory and commit to Local Repo

    $ cd proj1
    
    $ ll
    
    $ git status
    
    $ mkdir contacts
    
    $ cd contacts/
    
    $ vi names.txt # Add some names in the file
    
    $ cd ..
    
    $ git status
    
    $ git add . 
    
    $ git status
    
    $ git commit -m "contacts created"
    

#### Renaming a file using git

    $ git status
    
    $ ll
    
    $ git mv numbers.txt numbers2.txt
    
    $ git status

#### Removing a file using git 

    $ git rm contacts/names.txt
    
    $ git status

#### Commit Renamed and Removed files

    $ git commit -m "mv and rm commands"
    
    $ git status    
    
    $ ll
    
    $ git log

#### How to diff the workspace files 

    $ cat numbers2.txt
    
    $ echo "3" >> numbers2.txt
    
    $ git status
    
    $ git diff
    
    $ echo "4" >> numbers2.txt
    
    $ git diff
    
#### Staged area with diff command 

    $ git add numbers2.txt
    
    $ git diff
    
    $ git status
    
    $ git diff --staged
    
    $ git commit -m "changes"
    

#### Line by line tracking the changes

    $ cat numbers2.txt
    
    $ git blame numbers2.txt
    

#### Git Log with different options

    $ git log
    
    $ git log --oneline     # One line logs
    
    $ git log --author rns  # author based logs
    
    $ git log --author dev1
    
    $ git log numbers2.txt  # File based logs
    
    $ git log -n 2          # Number of latest commits
    
    $ git log ac9a0bc..cf336fa  # Between the commits
    

#### To trace the complete information of the commit

    $ git log | grep 284a00c
    
    $ git show 284a00cd6445bbad61e9d9d21aa22e09dd3abb84
    
    $ git show af12574
    
    
#### Cleaning dummy files

    $ git rm numbers2.txt
    
    $ git commit -m "deleted all files"
    
    $ ll


#### Create dummy project files

    $ mkdir src
    
    $ cd src/
    
    $ vi HelloWorld.java
    
    $ cd ..
    
    $ vi pom.xml
    
    $ ll
    
    $ git status
    
    $ git add .
    
    $ git commit -m "Java project created"
    
    $ git status
    

### GitHub (https://github.com/)

##### Go to GitHub and Signup the account

##### Create a Repository with b40project

##### Generate access token key 

      Click on User Profile -> Settings -> Developer Settings -> Personal Access Tokens -> Generate Token
      
##### Clone the Repository URL from Github

  
### Go back to EC2 instance


#### Add the remote repo to the current local repo

    $ git config --list
    
    $ git remote add origin https://github.com/venkat09docs/b40project.git
    
    $ git config --list
    

#### Remove it and observe the config properties then add it

    $ git remote remove origin
    
    $ git config --list
    
    $ git remote add origin https://github.com/venkat09docs/b40project.git
    
    $ git config --list
    
    $ git remote -v


#### Check the branch info

    $ git branch


#### Push the changes to the remote repo

    $ git push origin master


### Go to GitHub and check the latest changes in remote repo

##### edit pom.xml file in github itself and commit the changes

### Go back to EC2 instance


#### verify the local file of pom.xml

    $ cat pom.xml

#### Pull the latest changes from the Remote repo

    $ git pull origin master

    $ cat pom.xml
