# ferclager dotfiles

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

5.1. Configure git with your own information, and generate the SSH key
```zsh
git config --global color.ui true
git config --global user.name "YOUR NAME"
git config --global user.email YOUR@EMAIL.com
ssh-keygen -t rsa -C YOUR@EMAIL.com
```

5.2. You have to copy and paste the output of the following command and paste it [here](https://github.com/settings/ssh).
```zsh
cat ~/.ssh/id_rsa.pub
```

5.3. Update git configuration
```zsh
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
