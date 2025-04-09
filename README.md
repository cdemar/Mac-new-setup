# This is when I set up a new Mac

This is for future me when I factory set my Mac or when I buy a new Mac so I don't have to try and remember all of the things I care about in my Mac setup.

## Overview

### First thing after I make my account

- In System Settings
  - Check for software updates
  - Go to Touchpad and change from 'click' to 'tap to click'
  - Change the second click 'tap with 2 fingers' to 'click on bottom right'
  - Under 'Desktop and Dock' turn on 'Automatically hid and show Dock'

### Instal of these
- Go to the App Store and download
  - Password manager
  - Grammarly
  - join honey
  - Super Agent
  - Slack
  - Keynote
  - Numbers
  - Pages
- Install
    - [Homebew](https://brew.sh)
    - [Wezterm](https://wezterm.org)
    - [Zoom](https://www.zoom.com/home/)
    - [Thinkorswim](https://www.schwab.com/trading/thinkorswim?src=SEM&ef_id=CjwKCAjwktO_BhBrEiwAV70jXugWvsMCUYGdlPWhqeMQnGvYpXV2yYtSo8jd5OnZsIeASThueCghnBoCxuAQAvD_BwE:G:s&s_kwcid=AL!5158!3!736506540239!e!!g!!thinkorswim!22175113800!173441860319&keywordid=kwd-297695813001&gad_source=1&gbraid=0AAAAADhoFlmFows5fOgKcTRA4Yjn-QRrr&gclid=CjwKCAjwktO_BhBrEiwAV70jXugWvsMCUYGdlPWhqeMQnGvYpXV2yYtSo8jd5OnZsIeASThueCghnBoCxuAQAvD_BwE)
    - [Logos](https://www.logos.com)
    - [Chrome](https://www.google.com/chrome/)
- Install from brew spasificly
    - Python
    - Git
    - htop
        - to use this just type 'sudo htop'
    - font-meslo-lg-nerd-font
    - powerlevel10k
    - zsh-autosuggestions
    - zsh-syntax-highlighting
    - eza
    - nvim

### After you run all of these you will then want to test them out by doing these commands:
For 'htop'
```bash
sudo htop
```

For 'powerlevel10k
```bash
echo "source $(brew --prefix)/share/powerlevel10k/powerlevel10k.zsh-theme" >> ~/.zshrc
```

```bash
source ~/.zshrc
```

for 'zsh-autosuggestions'
```bash
echo "source $(brew --prefix)/share/zsh-autosuggestions/zsh-autosuggestions.zsh" >> ~/.zshrc
```
```bash
source ~/.zshrc
```

for 'zsh-syntax-highlighting'
```bash
echo "source $(brew --prefix)/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ~/.zshrc
```
```bash
source ~/.zshrc
```

### Now we are ready to start working on Wezterm and NeoVim
let us first start with getting the ~/.config available to be used as we will be putting some data inside that folder. We can see what the permissions level is by typing
```bash
ls -l ~/.config
```
We should see something like this
```diff
-rw-------  1 cdemar  staff  1234 Apr 4 12:00 wezterm.lua
```
If it says 'Permission denied, or if the file isn't readable, fix it with this
```bash
chmod 644 ~/.config/wezterm/wezterm.lua
```
That sets the file to be:
- Read/write for you
- Readable for WezTerm (which runs under your user account)
Now let's see if there is a folder in ~/.config named wezterm and another named nvim. If there is not then run the following code
```bash
mkdir -p ~/.config/wezterm
```
```bash
touch ~/.config/wezterm/wezterm.lua
```
```bash
mkdir -p ~/.config/nvim
```
```bash
touch ~/.config/nvim/init.lua
```

Now that we can make the folders let's first do the easier of the two out of the way first.
run this code to get into the wezterm folder then using nvim as our editor we can add code to make it look nicer.

```bash
cd ~/.config/wezterm
```
```bash
nvim wezterm.lua
```
