# PracticeField

# Show git branch name
mostrar_git_branch() {
     git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}
export PS1="\u@\h \[\033[32m\]\w\[\033[36m\]\$(mostrar_git_branch)\[\033[00m\] $ "
