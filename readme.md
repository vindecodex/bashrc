## Git Shortcuts
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

## Docker Shortcuts
[MyDucker](https://github.com/vindecodex/dockertips)
```bash
#mycustomDockerShortCuts
alias dbuild="docker-compose build"
alias drmserv="docker-compose rm -f -s -v $1"
alias dupserv="docker-compose -f docker-compose.yml up $1"
dockerup () {
  num=$1
  dbuild
  drmserv $1
  dupserv $1
}
```

## Creating a copy paste data with variable
`alias anyname="sed -n 's/^variable=//p' /.file | pbcopy"`

`alias anyname1="sed -n 's/^variable1=//p' /.file1 | pbcopy"`


### For New Device
- if you are using bash then create `.bashrc` on ~/
- if you are using zsh then create `.zshrc` on ~/

### Creating alias separate file
- Inside `.bashrc` or `.zshrc`
- source the alias file by `source ~/.your-alias` - this code must be inside `.bashrc` or `.zshrc`
