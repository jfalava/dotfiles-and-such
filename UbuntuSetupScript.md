# Ubnutu Setup Script

```sh
#/bin/sh
## Update Packages ##
sudo apt update -y && sudo apt upgrade -y
sudo apt install -y build-essential libssl-dev libffi-dev libbz2-dev libreadline-dev libsqlite3-dev zlib1g-dev libncurses5-dev libncursesw5-dev liblzma-dev libgdbm-dev libnss3-dev libedit-dev libcurl4-openssl-dev libxml2-dev libxslt1-dev curl git unzip wget zsh
## Homebrew ##
# Bash Shell Profile Edits #
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
(echo; echo 'eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"') >> ~/.bashrc
eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
source .bashrc
# Homebrew Packages #
brew install gcc
brew install golang
brew install node
brew install bat
brew install zoxide
brew install eza
brew install fastfetch
brew install ffmpeg
brew install zig
## Install OhMyPosh ##
sudo -S chsh -s $(which zsh) jfalava
curl -s https://ohmyposh.dev/install.sh | bash -s
brew install zsh-syntax-highlighting
brew install zsh-autosuggestions
## Alias Edits ##
cat <<EOF >> "$HOME/.zshrc"
## Paths
PATH=$PATH:/home/jfalava/go/bin
PATH=$PATH:/home/jfalava/.local/bin
export HOMEBREW_NO_AUTO_UPDATE=1
## Aliases
alias auto-update='sudo apt update && sudo apt upgrade && brew update && brew upgrade && brew cleanup'
alias git-name='git config user.name "Jorge Fernando Álava"'
alias git-email='git config user.email "git@jfa.dev"'
alias cls='clear'
alias ff='fastfetch'
alias l='eza --color=always --long --git --no-filesize --icons=always'
alias ls='eza --color=always --long --git --no-filesize --icons=always --all'
## Sources
eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
eval "$(oh-my-posh init zsh --config https://raw.githubusercontent.com/JanDeDobbeleer/oh-my-posh/refs/heads/main/themes/wopian.omp.json)"
source /home/linuxbrew/.linuxbrew/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
source $(brew --prefix)/share/zsh-autosuggestions/zsh-autosuggestions.zsh
EOF
```
