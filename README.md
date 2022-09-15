# git_practice

# ssh
git@github.com:redbull0425/git_practice.git

# https
https://github.com/redbull0425/git_practice.git


[more]
# …or create a new repository on the command line

echo "# git_practice" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/redbull0425/git_practice.git
git push -u origin main

[more]
# …or push an existing repository from the command line

git remote add origin https://github.com/redbull0425/git_practice.git
git branch -M main
git push -u origin main
