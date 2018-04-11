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
