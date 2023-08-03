# frclager dotfiles

## Steps to bootstrap a new Mac

1. Install Apple's Command Line Tools, which are prerequisites for Git and Homebrew.
```zsh
# Install Apple's Command Line Tools in your brand new Mac
xcode-select --install
```

2. Install sdkman.
```zsh
# Install sdkman
curl -s "https://get.sdkman.io" | bash
```

3. Install Homebrew.
```zsh
# Install Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

4. Install the software listed in Brewfile
```zsh
brew bundle --file ~/your_path/.dotfiles/Brewfile 
```
