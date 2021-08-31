# Get started Ubuntu for Software Development

Update packages

```bash
sudo apt update
sudo apt upgrade -y
```

Install Google Chrome

```bash
sudo wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt install ./google-chrome-stable_current_amd64.deb
cat /etc/apt/sources.list.d/google-chrome.list
google-chrome adonyssantos.me # this is a test
```

Install dev apps

```bash
# Visual Stuio Code
sudo apt install code

# Vim
sudo apt install vim

# Git
sudo apt install git

# Node & NPM
sudo apt install -y node npm

# Curl
sudo apt install -y curl snap

```

NVM - Node

```bash
# Install NVM
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
sudo shutdown -r 0
source ~/.profile

# Install Node
nvm install node

# List isntall versions
nvm ls

# Use a version
nvm use 12.18.3
```

Install ZSH & Git Core

```bash
# Install ZSH and Git Core
sudo apt-get install -y  zsh git-core
wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | zsh
chsh -s `which zsh`
sudo shutdown -r 0

# Install Fonts Powerline
sudo apt-get install fonts-powerline
nano ~/.zshrc

# Install ZSH Theme
sudo npm install -g spaceship-prompt
ZSH_THEME="spaceship"

# Install ZSH  Autocomplete
mkdir ~/.zsh
cd ~/.zsh
git clone --depth 1 -- https://github.com/marlonrichert/zsh-autocomplete.git
sudo shutdown -r 0
source ~/.zsh/zsh-autocomplete/zsh-autocomplete.plugin.zsh

# Install ZSH Autosuggestions
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions
sudo shutdown -r 0
source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh
```

Install Albert Launcher (Spotlight Search)

```bash
curl https://build.opensuse.org/projects/home:manuelschneid3r/public_key | sudo apt-key add -
echo 'deb http://download.opensuse.org/repositories/home:/manuelschneid3r/xUbuntu_20.04/ /' | sudo tee /etc/apt/sources.list.d/home:manuelschneid3r.list
sudo wget -nv https://download.opensuse.org/repositories/home:manuelschneid3r/xUbuntu_20.04/Release.key -O "/etc/apt/trusted.gpg.d/home:manuelschneid3r.asc"
sudo apt update
sudo apt install -y albert
```

Install Spotify

```bash
curl -sS https://download.spotify.com/debian/pubkey_0D811D58.gpg | sudo apt-key add - 
echo "deb http://repository.spotify.com estable no libre" | sudo tee /etc/apt/sources.list.d/spotify.list
sudo apt-get update && sudo apt-get install spotify-client

```

Install VLC Media Player

```bash
sudo apt install vlc
```

Install Discord

```bash
sudo apt update
sudo apt install -y gdebi-core wget
wget -O ~/discord.deb "https://discordapp.com/api/download?platform=linux&format=deb"
sudo gdebi ~/discord.deb
discord
```

Install others apps

```bash
sudo apt install -y telegram obs-studio
sudo apt install neofetch -y
sudo apt-get install audacity
```
