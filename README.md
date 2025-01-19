# My Dotfiles

Included tools:
- [Chezmoi](https://www.chezmoi.io/): Manages dotfiles.
- [Antidote](https://antidote.sh/): Manages ZSH Plugins.
- [Powerlevel10k](https://github.com/romkatv/powerlevel10k): Zsh Theme.
- [git-delta](https://dandavison.github.io/delta/): Syntax highlighting pager for git diffs, logs, etc.
- [zsh-z](https://github.com/agkozak/zsh-z) Quick directory navigation via "jumping".

## Packages to install

If on Arch Linux:
`sudo pacman -Syu && sudo pacman -S git git-delta open-ssh unzip zsh bat eza chezmoi`

If on Mac:
`brew install batcat chezmoi git-delta eza ...`

## Other Setup
- If setting up Arch on WSL, follow this tool for the basics: https://github.com/yuk7/ArchWSL
- Setup SSH keys for GitHub, and any other remotes. https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
- If on linux, then change the default shell to zsh with `chsh -s $(which zsh)`
- Install fonts for Powerlevel10k, and configure it: https://github.com/romkatv/powerlevel10k?tab=readme-ov-file
- Install a tool to manage Node and other tooling versions. Currently, I am trying out Mise: https://mise.jdx.dev/installing-mise.html

## Setting up Chezmoi

Once Git and the SSH keys are set up, you can setup the tools from this repo by doing:
```sh
chezmoi init git@github.com:JackRobards/dotfiles.git
chezmoi apply -v
```
