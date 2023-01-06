# .dotfiles
Configuration files for my personal dev machine

```shell
# Add symlinks
ln -s ~/dev/.dotfiles/.zshrc ~/.zshrc
ln -s ~/dev/.dotfiles/.p10k.zsh ~/.p10k.zsh
ln -s ~/dev/.dotfiles/.config ~

# Installing Node.js --
# NVM:
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
nvm install --lts
npm i -g typescript
npm i -g ts-node
```