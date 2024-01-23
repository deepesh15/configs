## Git Helper functions
```
git_current_branch() {
  cat "$(git rev-parse --git-dir 2>/dev/null)/HEAD" | sed -e 's/^.*refs\/heads\///'
}
```

## GIT ALIASES
```
alias gs='git status'

alias gae='git add .' #git add everything

alias gco='f() { 
              git checkout $@; 
            }; f'

alias gst='git stash'
alias gstp='gst pop'
alias gstl='gst list'

alias gpl='git pull'
alias gplo='f() {
  gpl origin $1;
}; f'

alias gp='git push'
alias gpthis='gp origin $(git_current_branch)'
alias gpthis!='gp --set-upstream origin $(git_current_branch)'

alias gcm='git commit -am'

alias gf='git fetch'
```
