# After install Mac OS

Download and install Google Chrome and Visual Studio Code:

- https://code.visualstudio.com/download
- https://www.google.com/intl/pt-BR/chrome/

Open the terminal and run:

```
xcode-select —install
```

Install Homebrew:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Install Oh-my-ZSH!

```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# Spaceship prompt
git clone https://github.com/spaceship-prompt/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1

ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"

# ZSH Syntax highlighting
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

# ZSH Autosuggestions
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

# Powerline fonts
git clone https://github.com/powerline/fonts.git --depth=1
cd fonts
./install.sh
cd ..
rm -rf fonts
```

Change `~/.zshrc` "plugins" and "ZSH_THEME" to be like:
nano ~/.zshrc

ZSH_THEME="spaceship"
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)


```
...
ZSH_THEME="spaceship"
...
plugins=(git zsh-syntax-highlighting zsh-autosuggestions)
...
```

Install iTerm2 and Python 3.10 (optional)

```
brew install iterm2 python@3.10
brew install python-tk@3.10

export PATH="/usr/local/opt/python@3.10/bin:$PATH"
export LDFLAGS="-L/usr/local/opt/python@3.10/lib"
```
