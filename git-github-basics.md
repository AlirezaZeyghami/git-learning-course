# Git & GitHub Basics

## 🔑 SSH Setup
- **SSH (Secure Shell)**
- remote vs local
- Public key / Private key

```bash
ssh-keygen

----
Add SSH key to GitHub
----

GitHub >> Settings >> SSH and GPG keys >> New SSH key

In Git Bash:

cd ~/.ssh
cat id_ed.pub

Copy → Paste → Add

In case of error with agent:
eval $(ssh-agent -s)
ssh-add id_ed

----
🌍 Remote
----

Git is distributed → it can have multiple remotes.

git remote
git remote add origin git@github.com:AlirezaZeyghami/git-learning-course.git
git push origin master
git push -u origin master

git remote
git remote add origin git@github.com:AlirezaZeyghami/git-learning-course.git
git push origin master
git push -u origin master

git fetch → safe command

git pull → merge origin with local

git push

----
🛠️ IDE Integration
----

VSCode linking to GitHub

PyCharm linking to GitHub

Commit shortcut: Ctrl + K

----
🌿 Branching
----

git branch
git checkout
git checkout -b feature-1
git push -u origin feature-1
git checkout master   # switch branch
