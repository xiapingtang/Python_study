#generate new key pair
ssh-keygen -t rsa -C "tangxiaping@gmail.com" -f 'id_rsa_GitHub'
# change config file for new key
vi ~/.ssh/config
#add new key to ssh key chain
ssh-add -K ~/.ssh/id_rsa_GitHub 
# list the ssh key chain
ssh-add -L
# link remote repo to existing working directory
git remote add origin git@github.com:xiapingtang/Python_study.git

# point HEAD to a different version like a time machine
git reset --hard commit_id/HEAD^/HEAD^^
# show the difference between file in working directory and that in master branch
git diff HEAD -- 'file' 
# checkout file in repository to the working directory
git checkout -- 'file'
# update the file in repository with the latest version
git reset HEAD 'file' 
# create new branch and point to the new branch
git checkout -b 'branch'
# remove branch
git branch -d 'branch'
# merge 'branch' to current branch
git merge 'branch'
# history for version control including future commit
git reflog

# record file change in working directory to stage zone of repository
git add 'file'
# commit file change in stage zone to master branch of repository
git commit -m 'message'
# list current branch
git branch
# remove committed file
git rm 'file'
# history for version control
git log
# file status of git directory
git status

