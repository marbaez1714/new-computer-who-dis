# New-Computer-Who-Dis

> Updated 7/8/2022

> Check out the `dotfiles` directory to see how my configs look after the initial setup.

_Setting up a new computer can be a pain so let me show you how I did it on my new personal machine!_

## Resources:

- [Guide to iTerm2](https://medium.com/featurepreneur/guide-to-iterm2-46cd4625d55a)

## Guide

1. Installed [**Google Chrome**](https://www.google.com/chrome/)
2. Installed [**Homebrew**](https://brew.sh/)

   1. `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
   2. `echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/mario/.zprofile`
   3. `eval "$(/opt/homebrew/bin/brew shellenv)"`

3. Installed [**iTerm2**](https://iterm2.com/)

   - `brew install --cask iterm2`

4. Installed [**zsh**](https://www.zsh.org/)

   - `brew install zsh`

5. Installed [**Oh My Zsh**](https://ohmyz.sh/)

   - `sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
   - `chsh -s $(which zsh)`

6. Installed **tree** (makes pretty directory lists)

   - `brew install tree`

7. Installed [**Powerlevel10k**](https://github.com/romkatv/powerlevel10k) (it's a cool theme)

   1. `git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k`
   2. Set `ZSH_THEME="powerlevel10k/powerlevel10k"` in `~/.zshrc`
   3. When you open the terminal, it will start the install wizard.

      - MAKE SURE YOU SELECT YES TO INSTALL FONTS OR THINGS GET WEIRD

8. Installed [**nvm**](https://github.com/nvm-sh/nvm)

   - `brew install nvm`
   - Add `nvm` to `plugins` array in `~/.zshrc`
   - Restart terminal and run `nvm ls` to make sure it is installed

9. Installed [**node**](https://nodejs.org/en/)

   - `nvm install node`
   - Ran `node -v` to ensure the install ran correctly (currently installed v18.5.0)
   - Add `node` to `plugins` array in `~/.zshrc`

10. Installed [**VSCode**](https://code.visualstudio.com/)

    - Used the normal download from https://code.visualstudio.com/
    - Open the command palette and run `Shell Command: Install 'code' command in PATH` (gives VSCode terminal access)
    - Add `vscode` to `plugins` array in `~/.zshrc`
    - If you have your VSCode settings set to sync, log in and sync your settings!

11. Installed [**Github CLI**](https://cli.github.com/)

    - `brew install gh`
    - Added ssh key by running `gh auth login -p ssh` (will open browser to authenticate)

12. Installed [**yarn**](https://classic.yarnpkg.com/en/)

    - `brew install yarn`
