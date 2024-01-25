# CREATE SSH KEYS FOR GIT

ssh-keygen -t rsa -C "example@email.com"

# BASIC CONFIGURATION

git config --global user.name “Name Surname”
git config --global user.email “example@email.com”
git config --global core.editor "vim"
git config --global color.diff auto
git config --global color.status auto
git config --list --show-origin

# BASIC COMMANDS

git remote -v
git status
git add __filename__
git commit -m "commit message"
git log
git push
git blame __filename__
git fetch
git merge

git checkout -- __filename__
git checkout .
git clean -xdf

git reset HEAD^^ ==(HEAD~2) ^^ or ~2 = number of the commits==
git reset -- __filename__

# BRANCHING

git branch -b __branch_name__  ==create branch branch_name and checkout to this branch==
git branch __branch_name__  ==checkout to branch_name==
