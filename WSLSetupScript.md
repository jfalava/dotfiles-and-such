# WSL

## One-click setup script

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
brew install zenith
brew install bat
brew install zoxide
brew install eza
brew install fastfetch
brew install ffmpeg
brew install optipng
##
echo "1234" | sudo -S chsh -s $(which zsh) jfalava
curl -s https://ohmyposh.dev/install.sh | bash -s
(echo; echo 'PATH=$PATH:/home/jfalava/go/bin') >> ~/.zshrc
eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
(echo; echo 'eval "$(oh-my-posh init zsh --config '/mnt/c/Users/jfalava/AppData/Local/Programs/oh-my-posh/themes/wopian.omp.json')"') >> ~/.zshrc
(echo; echo 'PATH=$PATH:/home/jfalava/.local/bin') >> ~/.zshrc
brew install zsh-syntax-highlighting
brew install zsh-autosuggestions
(echo; echo 'source /home/linuxbrew/.linuxbrew/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh') >> ~/.zshrc
(echo; echo 'source $(brew --prefix)/share/zsh-autosuggestions/zsh-autosuggestions.zsh') >> ~/.zshrc
(echo; echo 'eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"') >> ~/.zshrc
(echo; echo 'export HOMEBREW_NO_AUTO_UPDATE=1') >> ~/.zshrc
## Alias Edits
cat <<EOF >> "$HOME/.zshrc"
alias auto-update='sudo apt update && sudo apt upgrade && brew update && brew upgrade && brew cleanup'
alias git-name='git config user.name "Jorge Fernando Álava"'
alias git-email='git config user.email "git@jfa.dev"'
alias cls='clear'
alias ff='fastfetch'
alias l='eza --color=always --long --git --no-filesize --icons=always'
alias ls='eza --color=always --long --git --no-filesize --icons=always --all'
EOF
```

```sh
source .zshrc
```
