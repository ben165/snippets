BASHRC


PS1="$ "

tit() {
  PS1=$1": "
}

title () {
  echo -en "\033]0;$1\007"
}

# CHANGE
export PATH="$PATH:$HOME/b"

alias l='ls -CF --color=never'
alias ll='ls -alFh --color=never -v' #h
alias t="tmux"
alias tm="tmux attach-session -t "
alias bc='bc -lq'
alias tree='tree --charset=ascii'
alias off='rfkill block wlan'
alias on='rfkill unblock wlan'
alias gpg0='gpg -er Ange8899'
alias hd='hunspell -d de_DE'
alias he='hunspell -d en_US'
alias fd="fdfind -i"
alias bigger='find . -type f -exec du -h {} + | sort -rh | head -n 25'
alias diff='git diff --no-index'
alias gb='visualboyadvance-m'
alias pm='podman'

d=$(date +%y-%m-%d)
alias istall='sudo dpkg -i'

#PROGRAMS
alias c='clear'
alias x='exit'
alias h='cd ~/'
alias p='python -q'
alias pp='python3 -q'
alias p3='pushd ~/temp/;source p3/bin/activate;popd;'
alias p3d='deactivate;'
alias json='python3 -m json.tool'
alias pwc='pwd | tr -d "\n" |cv'
alias tt='tr " " "-"'
alias bb='source ~/.bashrc'
alias zz='source ~/.zshrc'
alias jflap='java -jar ~/Downloads/Jflap.jar'
alias flow='cd ~/w/CHECKOUT/lidlRequests/flow'

#MAC files
#alias ds="find ./ -name ".DS_Store" -exec echo {} \;"
alias ds='find ./ -name ".DS_Store" -delete'
#alias mong='echo -e "docker exec -it mongo bash\nmongosh --username root --password root --host localhost --authenticationDatabase admin"'


alias gitt='git add .; git commit -m "update";'
alias gitn='git branch --show-current'
alias gits='git status'
alias gitp='git pull'
alias gitl='git log --oneline'
alias gitsave='git archive --format=tar HEAD > code.tar'
alias gitd='git diff --name-only main...'
alias gitc='git checkout'
alias gitr='git restore --source main --worktree'
alias co='./gradlew build --dependency-verification off'
alias bo='./gradlew bootrun --dependency-verification off'
alias ctest='rm -rf ~/temp/test; cp -r build/reports/tests/test ~/temp/'

alias m1='git restore --source main --worktree src/main/resources/application-local.yml'
alias t1='git restore --source test --worktree src/main/resources/application-local.yml'
alias r1="git restore src/main/resources/application-local.yml"



pushd ~/temp/;source p3/bin/activate;popd;

encrypt() {
  openssl enc -aes-256-cbc -salt -pbkdf2 -md sha256 -in "$1" -out "$1.enc"
}

decrypt() {
  openssl enc -d -aes-256-cbc -pbkdf2 -md sha256 -in "$1" -out "${1%.enc}"
}








ZSHRC
PS1="$ "

tit() {
  PS1=$1": "
}

title () {
  echo -en "\033]0;$1\007"
}

# Change
export PATH="$PATH:$HOME/b"


alias l='ls -CF --color=never'
alias ll='ls -alFh --color=never -v' #h
alias t="tmux"
alias tm="tmux attach-session -t "
alias tree='tree --charset=ascii'
alias off='rfkill block wlan'
alias on='rfkill unblock wlan'
#d=$(date +%y-%m-%d)
alias istall='sudo dpkg -i'

#MAC
setopt RM_STAR_SILENT


#PROGRAMS

alias hunspelld='hunspell -d de_DE'
alias c='clear'
alias x='exit'
alias h='cd ~/'
alias p='python -q'
alias pp='python3 -q'
alias p3='source ~/p3/.venv/bin/activate'
alias p3d='deactivate;'
alias json='python3 -m json.tool'
alias pwc='pwd | tr -d "\n" |cv'
alias tt='tr " " "-"'
alias bb='source ~/.bashrc'
alias zz='source ~/.zshrc'
alias jflap='java -jar ~/Downloads/Jflap.jar'
alias flow='cd ~/w/CHECKOUT/lidlRequests/flow'
alias bigger='find . -type f -exec du -h {} + | sort -rh | head -n 25'
alias diff='git diff --no-index'

alias ds='find ./ -name ".DS_Store" -delete'

alias gitt='git add .; git commit -m "update";'
alias gitn='git branch --show-current'
alias gits='git status'
alias gitp='git pull'
alias gitl='git log --oneline'
alias gitsave='git archive --format=tar HEAD > code.tar'
alias gitd='git diff --name-only main...'
alias gitc='git checkout'
alias gitr='git restore --source main --worktree'
alias co='./gradlew build --dependency-verification off'
alias cox='./gradlew build --dependency-verification off -x test'
#alias co='./gradlew build --dependency-verification off -PdependencyLocking.overrideBuildEnvironment=true'
alias lk='./gradlew dependencies --write-locks'
alias vf='./gradlew --write-verification-metadata pgp,sha256 --export-keys'
alias bo='./gradlew bootrun --dependency-verification off'

alias m1='git restore --source main --worktree src/main/resources/application-local.yml'
alias t1='git restore --source test --worktree src/main/resources/application-local.yml'
alias r1="git restore src/main/resources/application-local.yml"


encrypt() {
  openssl enc -aes-256-cbc -salt -pbkdf2 -md sha256 -in "$1" -out "$1.enc"
}

decrypt() {
  openssl enc -d -aes-256-cbc -pbkdf2 -md sha256 -in "$1" -out "${1%.enc}"
}
