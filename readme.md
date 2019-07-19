```bash
alias atwiki="cd ~/dev/go/src/bitbucket.org/atfreaks/v3-top.atwiki.jp"
alias gs="git status"
alias gpom-rb="git pull origin master --rebase"
alias ga="git add ."
alias gaa="git add -A"
alias gc="git commit -m $1"
alias gl="git log"
alias gb="git checkout -b $1"
alias gco="git checkout $1"
gpo() {
  branch=`git branch | grep \* | cut -d ' ' -f2`
  git push origin $branch $1
}
grebase () {
  num=$1
  git rebase -i HEAD~$num
}
```
