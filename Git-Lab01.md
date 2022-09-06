# Launch the EC2 Instance

# Install the Git and check Version
  $ git --version
  $ sudo yum install git -y
  $ git --version
  $ which git

# Git Help commands
  $ git --help
  $ git help -a
  $ git clone --help
  $ man git-clone
  
# Set the git configuration at globally
  $ git config --global --list
  $ git config --global user.name "rnstech"
  $ git config --global user.email "rnstech@gmail.com"
  $ git config --global --list
  $ cat /home/ec2-user/.gitconfig

# Create existing directory as a Git repo
  $ mkdir proj1
  $ cd proj1/
  $ ll -la
  $ git init
  $ ll -la
  $ ll .git/
  $ cd ..

# Creating New Git Repo
  $ git init proj2
  $ ll
  $ ll -la proj2/
  $ cd proj1
  $ ls -lrth
  $ ls -lrtha

# Checking Git Global and project scope properties
  $ git config --global --list
  $ git config --list

# Adding files in workspace and staging it
  $ vi numbers.txt # add Number 1 in the file
  $ ll
  $ git status
  $ ll
  $ git add numbers.txt
  $ git status

# From staging area restore it to workspace
  $ git rm --cached numbers.txt
  $ git status

# Staging, committing and check the logs
  $ git add numbers.txt
  $ git status
  $ git commit -m "Created number file"
  $ git status
  $ git log
  $ git status

# Revert back the changes from work dir
  $ echo "2" >> numbers.txt
  $ git status
  $ cat numbers.txt
  $ git restore numbers.txt
  $ cat numbers.txt

# Staging files revert back to workspace and then rollback the changes
  $ echo "2" >> numbers.txt
  $ git status
  $ git add numbers.txt
  $ git status
  $ git restore --staged numbers.txt
  $ git status
  $ git restore numbers.txt
  $ cat numbers.txt

# Staging, committing and check the logs
  $ echo "2" >> numbers.txt
  $ git add .
  $ git status
  $ git commit -m "Added number 3"
  $ git log

# Staging, committing and check the logs
  $ echo "3" >> numbers.txt
  $ git status
  $ git commit -a -m "Number 3 added"
  $ git status
  $ git log

# while committing give proper comment on the basis Ticket #
  $ vi numbers.txt # Remove 3
  $ git status
  $ cat numbers.txt
  $ git add .
  $ git commit -m "Jira#123 removed Number 3"
  $ git log
