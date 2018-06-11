# Installations

## Install OhMyZsh
- Installed 'zsh' for the terminal: http://ohmyz.sh/
  - if install didn't working, fixed problem by activating the editor using this command: `chsh -s /bin/zsh`

## Install Atom
- Installed atom: https://atom.io/
  - In 'Atom' click 'Atom' on top left corner and hit 'Install Shell Commands' <-- Very important!!

## Install Homebrew
- Installed homebrew: https://brew.sh/
    - `brew install tree` to see the folder structure

## Install Anaconda Python Distribution

- Install Anaconda: https://www.anaconda.com/download/#macos
  - Use Python 3.6 version

Since you installed Z-shell (ZSH) but Ananconda defaults to the Bourne again shell (BASH), it added to the file that gets run every time you start your terminal, the `~/.bash_profile` file, but ZSH doesn't know about this file, only BASH does. So edit your `~/.zshrc`, e.g. by typing `atom ~/.zshrc` on the command line, and press enter a few times to add new lines, then add the text sso the very very first line is:

```
source ~/.bash_profile
```

This will run EVERYTHING in your `~/.bash_profile` when you open a new terminal tab or window. So to activate it, open a new tab (Command-T just like in Chrome or Safari) and close your old one.
