# 1. Install git on your machine
You can follow this [link](https://git-scm.com/download/) to install git.
```
git --version
```
Finally, you can use this to check whether git is installed successfully.

# 2. Add your account on your machine
Set up your identity.
```
git config --global user.name "your name"
git config --global user.email "your mail"
```
Then check your settings.
```
git config --list
```

# 3. Set your SSH Pub Key to your Github
If you have not set SSH Pari, you can use this to set up your SSH Pair.
```
ssh-keygen -t rsa -C xx@qq.com
```
Then, select Settings -> SSH and GPG Keys -> New SSH Key in github. Add your SSH Public Key in it.

Use this to check your connection to github.
```
ssh -T git@github.com
```

# 4. Create and push a repository 
At first, you must create a repository on github manually.

Then you can create a new repository on the command line locally.
```
echo "# go_learn" >> README.md  
git init  
git add README.md  
git commit -m "first commit"  
git branch -M main  
git remote add origin https://github.com/YourName/YourRepositoryName.git  
git push -u origin main  
```
  
…or push an existing repository from the command line
```
git remote add origin https://github.com/YourName/YourRepositoryName.git  
git branch -M main  
git push -u origin main  
```