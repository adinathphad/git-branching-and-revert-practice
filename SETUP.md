# Complete Project Setup (Single Flow)

Run the following commands in order:

```bash
mkdir myrepo
cd myrepo

git init

git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"

touch newfile
git add newfile
git commit -m "Initial commit - added newfile"

git checkout -b my1stbranch

echo "This is some text" >> newfile
touch readme.md
git add .
git commit -m "Modified newfile and added readme.md"

git revert HEAD --no-edit

touch goodfile
git add goodfile
git commit -m "Added goodfile"

git log

git checkout master
git merge my1stbranch

git branch -d my1stbranch

git remote add origin https://github.com/YOUR_USERNAME/git-branching-and-revert-practice.git
git push -u origin master
