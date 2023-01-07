# .dotfiles
Configuration files for my YouTube dev machine

```shell
# Kitty terminal
curl -L https://sw.kovidgoyal.net/kitty/installer.sh | sh /dev/stdin

# Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# oh-my-zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# powerlevel10k
# Step 1:
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
# Step 2: Set ZSH_THEME="powerlevel10k/powerlevel10k" in ~/.zshrc
# Step 3: Configure - either open a new tab or run:
p10k configure

# Kitty colour theme
kitty +kitten themes

# Install Git
brew install git

# Install apps
brew install --cask visual-studio-code
brew install --cask flycut
brew install --cask keepingyouawake

# Create dev directory
mkdir dev
cd dev

# Create config directory (equivalent of this repo)
mkdir .dotfiles
cd .dotfiles

# Move dev config files to new directory
mv ~/.zshrc ~/dev/.dotfiles
mv ~/.p10k.zsh ~/dev/.dotfiles
mv ~/.config ~/dev/.dotfiles 

# Add symlinks
ln -s ~/dev/.dotfiles/.zshrc ~/.zshrc
ln -s ~/dev/.dotfiles/.p10k.zsh ~/.p10k.zsh
ln -s ~/dev/.dotfiles/.config ~

# Store repo remotely
# Add ssh key for machine to remote host if desired (follow video for instructions)
git init
git add .
git commit -m "Initial commit"
git remote add origin insert_remote_host_url_here
git branch -M main
git push -u origin main

# Installing Node.js --
# NVM:
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
nvm install --lts
npm i -g typescript
npm i -g ts-node

# Install VSCode
brew install --cask visual-studio-code
```