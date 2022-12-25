# ubuntu

## vpn
```properties
# ~/.bashrc
export http_proxy=http://192.168.1.172:10811
export https_proxy=http://192.168.1.172:10811
```

```properties
# ~/.zshrc
export http_proxy=http://192.168.1.172:10811
export https_proxy=http://192.168.1.172:10811
```

## oh-my-zsh
```properties
# install zsh
sudo apt install zsh
zsh --version
chsh -s $(which zsh)
logout
echo $SHELL
```
```properties
# install oh-my-zsh and plugins
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

```

```properties
# ~/.zshrc
plugins=(
        git
        sudo
        extract
        zsh-autosuggestions
        zsh-syntax-highlighting
        )

ZSH_THEME="powerlevel10k/powerlevel10k"

POWERLEVEL9K_{LEFT,RIGHT}_SEGMENT_SEPARATOR

```