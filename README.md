# linux-setup

The following is a short overview over my usual linux setup, e.g packages and the like.

## Gnome interface

![Home Screen](imgs/screen.png?raw=true "Dekstop")

Usually kept with the dark theme and some gnome extensions.

To install gnome extensions you need the manager installed:
```bash
sudo apt install gnome-shell-extension-manager
```

Then the following packages I use is:

- Dash to Panel - An extension that makes it possible to have the menu bar at the top of the screen.

## Terminal

![Terminal](imgs/terminal.png?raw=true "Terminal")

I use Zsh + Oh my Zsh + powerlevel10k as my current terminal setup. This can be setup in the following steps.


### Zsh

Install Zsh:
```bash
sudo apt-get install zsh
```

Make zsh default:
```bash
chsh -s $(which zsh)
```

Then log out and in again, this should now have taken effect.

### Oh my Zsh

Next we install Oh my Zsh:
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Then install the following packages:

- [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions?ref=catalins.tech)
  A plugin giving auto suggestions as you write
  ```bash
  # To install
  git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
  ```
  Then add `zsh-autosuggestions` to plugins in .zshrc
- [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting?ref=catalins.tech)
  A plugin for syntax highlighting
  ```bash
  git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
  ```
  Then add `zsh-syntax-highlighting` to plugins in .zshrc
- [zsh-you-should-use](https://github.com/MichaelAquilina/zsh-you-should-use?ref=catalins.tech)
  A plugin for reminding you of command aliases
  ```bash
  git clone https://github.com/MichaelAquilina/zsh-you-should-use.git $ZSH_CUSTOM/plugins/you-should-use
  ```
  Then add `you-should-use` to plugins in .zshrc
- [zsh-bat](https://github.com/MichaelAquilina/zsh-you-should-use?ref=catalins.tech)
  A plugin for reminding you of command aliases
  ```bash
  # First ensure bat is installed
  sudo apt-get install bat
  # then install plugin
  git clone https://github.com/fdellwing/zsh-bat.git $ZSH_CUSTOM/plugins/zsh-bat
  ```
  Then add `zsh-bat` to plugins in .zshrc

### Powerlevel10k

Before powerlevel10k is to be install we setup terminal preferences:

- Choose a color scheme by the help of [Gogh](https://github.com/Gogh-Co/Gogh)
- Install all the fonts inside `fonts` folder, then in `terminal preferences` change font to `MesloLGS NF`

Then install [Powerlevel10k](https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#meslo-nerd-font-patched-for-powerlevel10k) with the following command:
```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

Then the next time you open the terminal the p10k configuration should start, if it does not then run the command:
```bash
p10k configure
```

### Other Cool Packages

List of other linux packages:

- Texlive - latex compiler
  ```bash
  sudo apt install texlive-full texlive-latex-recommended
  ```
- Texstudio - latex compiler
  ```bash
  sudo apt install texstudio
  ```
- Brave - browser
  ```bash
  sudo apt-get install brave
  ```
- Nordpass - password manager
  ```bash
  sudo snap install nordpass
  ```
- Emacs - Text editor
  ```bash
  sudo apt-get install emacs
  ```
  See my personal emacs setup [here](https://github.com/odeter/emacs)
