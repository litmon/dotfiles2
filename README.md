# Information

In this repository, I will manage my settings. see details below

- my dotfiles
- how to install tools, applications


# how to setup my macbook

## import terminal settings

open `Terminal.app`, and settings > profiles.

click "⚙" icon and choose import settings.

then, open `mon-pro.terminal` file in this repository


## xcode-select install, setup git

```
xcode-select install
```

## Java



## Homebrew

https://brew.sh/index_ja

run the below script, you could install homebrew.

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## zsh

```
chsh -s /usr/bin/zsh

# or use zsh installed from brew
brew install zsh
sudo echo "/usr/local/bin/zsh" >> "/etc/shells"
chsh -s /usr/local/bin/zsh
```

## prezto

prezto is the configuration framework for zsh. (https://github.com/sorin-ionescu/prezto)

```
git clone --recursive https://github.com/sorin-ionescu/prezto.git "${ZDOTDIR:-$HOME}/.zprezto"
setopt EXTENDED_GLOB
for rcfile in "${ZDOTDIR:-$HOME}"/.zprezto/runcoms/^README.md(.N); do
  ln -s "$rcfile" "${ZDOTDIR:-$HOME}/.${rcfile:t}"
done
```

if you run the script before put my dotfiles, you should overwrite an existing dotfiles with my dotfiles.

## vim

TBD

## ruby

install ruby through rbenv.

```
brew install rbenv
rbenv install -l # show ruby versions
rbenv install <version>
rbenv rehash
```

if you use japanese in pry-console, you should install ruby using readline, openssl.

```
brew install openssl
brew link openssl

brew install readline
CONFIGURE_OPTS="--with-readline-dir=/usr/local/opt --with-openssl-dir=/usr/local/opt" rbenv install <version>
rbenv rehash
```

## node.js

install node.js through nodebrew. (https://github.com/hokaccha/nodebrew)

```
curl -L git.io/nodebrew | perl - setup
nodebrew install <version>
nodebrew use <version>
```

