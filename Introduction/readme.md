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
git checkout -b 'new'
# create new branch from remote repository
git checkout -b new origin/new
# remove branch
git branch -d 'branch'
# merge 'branch' to current branch with fast-forward method
git merge 'branch'
# merge without fast-forward method
git merge --no-ff 'branch'
# push local master branch to remote origin branch
git push origin master
# set up tracking information between remote and local branch
git branch --set-upstream branch-name origin/branch-name

# save a snapshot of current file status
git stash
# list all the saved snapshot
git stash list
# recover the saved snapshot "ss1"
git stash apply 'ss1'
# delete the snapshot "ss1"
git stash drop 'ss1'
# recover the saved snapshot 'ss1' and then delete it
git stash pop 'ss1'

# create tag with name v0.1 and "message" for "commit id"
git tag -a v0.1 -m "message" "commit id" 
# delete tag v0.1
git tag -d v0.1
# push tag v1.0 to remote repository origin
git push origin v1.0
# push all tags to remote repository origin
git push origin --tags
# remove tag v0.9 in remove repository origin
git push origin :refs/tags/v0.9
# show the detail for tagged commit v0.1
git show v0.1

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
# history for version control including future commit
git reflog
# file status of git directory
git status
# create .gitignore file for default untracked files
see template at https://github.com/github/gitignore
# define alias for git which is recored in ~/.gitconfig
git config --global alias.st status
