# macOS Setup Guide for Frontend

> Phodal HUANG's macOS setup guide.

1. Install Xcode
2. Download Apps (WeChat, [JetBrains Toolbox](https://www.jetbrains.com/toolbox/app/?fromMenu), [Adobe Creative Cloud](https://www.adobe.com/creativecloud/desktop-app.html))
3. Install HomeBrew

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

4. Install brew Casks


```
brew cask install google-chrome
brew cask install iterm2 sublime-text sourcetree alfred
```

JDK

```
brew tap caskroom/versions
brew cask install java8
```

some tools

```
brew install wget nvm gradle git-extras scrcpy coreutils gnu-sed  —with-default-names
```

Daily

```
brew cask install neteasemusic sketch thunder firefox qq baiducloud
```

```
brew cask install virtualbox shadowsocksx charles
```

## NVM

```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash
```

config

```
export NVM_DIR="${XDG_CONFIG_HOME/:-$HOME/.}nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

## ZSH

change shell

```
brew install zsh
chsh -s /bin/zsh
```

### Oh-my-zsh

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

### Zsh AutoSuggestions

1.clone

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions
```

2.source

```
source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh
```


## Emacs

install

```
brew install emacs --HEAD  --with-gnutls --with-cocoa --with-mailutils  --with-librsvg --with-ctags --without-libxml2 --with-modules --with-imagemagick@6
```

config

```
git clone https://github.com/purcell/emacs.d.git ~/.emacs.d
````

## iOS

```
brew install libimobiledevice carthage --HEAD 
```

## Tools

```
brew cask install cheatsheet
```

## Android

```
export ANDROID_HOME=/Users/fdhuang/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools
```

add in ``local.properties``

```
sdk.dir=/Users/fdhuang/Library/Android/sdk
```

## Markdown

1. Download [MacTex](http://www.tug.org/mactex/mactex-download.html)

```
brew install pandoc make
```

## Git Config

```
git config --global user.email "h@phodal.com"
git config --global user.name "Phodal HUANG"
```


Keychain Access for TWO-Factor

Get Token: [Personal access tokens](https://github.com/settings/tokens)

### GPG

1. install tools

```
brew install gnupg pinentry-mac
```

2. create key

```
gpg --gen-key
```

```
gpg --list-secret-keys --keyid-format LONG 
```

results

```
sec   rsa2048/5C3D8793775E8537 2019-01-19 [SC] [expires: 2021-01-18]
      5BF2EA24922B8C14460552855C3D8793775E8537
uid                 [ultimate] Phodal HUANG <h@phodal.com>
ssb   rsa2048/4E30E78BB8B2E2E8 2019-01-19 [E] [expires: 2021-01-18]
```

3. config

```
git config --global user.signingkey 5C3D8793775E8537
git config --global commit.gpgsign true
```

tools

open ``~/.gnupg/gpg-agent.conf`` with:

```
pinentry-program /usr/local/bin/pinentry-mac
```

4. export 

copy key:

```
gpg --armor --export 5C3D8793775E8537 | pbcopy
```

input:

[GPG Keys](https://github.com/settings/keys)


## Image

图片转换

```
brew install imagemagick gs
```

矢量

```
brew install potrace
```

## Docker

```
brew install kitematic
```


## Quicklook

[Plugins](https://github.com/sindresorhus/quick-look-plugins)


```
brew cask install qlcolorcode qlstephen qlmarkdown quicklook-json qlimagesize webpquicklook suspicious-package quicklookase qlvideo
```

## Cisco Scripts


```
brew install oath-toolkit
```



