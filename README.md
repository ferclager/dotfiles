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

5. Update git configuration
```zsh
git config --global core.pager diff-sofancy | less --tabs=4 -RFX
git config --global color.ui true
git config --global color.diff-hifhlight.oldnormal red bold
git config --global color.diff-hifhlight.newnormal green bold
git config --global color.diff.meta yellow
git config --global color.diff.frag magenta bold
git config --global color.diff.commit yellow bold
git config --global color.diff.old red bold
git config --global color.diff.new green bold
git config --global color.diff.whitespace red reverse
git config --global push.default matching
```
