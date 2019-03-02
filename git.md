## All git commands

#### Setup remote git to an existing project
```
$ git remote add origin <repo-url>
$ git push -u origin master
$ git pull origin master
```
#### git alias commands
```
$ git config --global alias.co checkout
$ git config --global alias.br branch
$ git config --global alias.ci commit
$ git config --global alias.st status
```
#### linux alias for git commands
Add to bashrc (simiar file)
```
alias g.c='git co'
alias g.ca='git commit --amend --no-edit'
alias g.master='git co master'
alias g.p='git push'
alias g.cb='git rev-parse --abbrev-ref HEAD' # git current branch 
alias g.push-amend='git push origin $(g.cb) --force-with-lease'
alias g.push-u='git push -u origin $(g.cb)'
alias g.s='git status'
```
