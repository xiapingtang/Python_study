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

# put file change in working directory to stage zone
git add 'file'

# commit file change in stage zone to master branch
git commit -m 'message'

#point HEAD to a different version like a time machine
git reset --hard commit_id/HEAD^/HEAD^^

#file status of git directory
git status

#history for version control
git log

#history for version control including future commit
git reflog

# show the difference between file in working directory and that in master branch
git diff HEAD -- 'file' 
