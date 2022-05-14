# 클린 설치 후 세팅

## Homebrew
설치
```
-- Xcode 이때 설치 됨.
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

brew update

/****************** Dev Tools ********************/

brew install git iterm2 docker docker-compose node vnm openjdk@8 openjdk@11 curl

brew install --cask google-chrome slack postman dbeaver-community intellij-idea visual-studio-code github

/************* 단축어 *************/
echo "alias ll='ls -al'" > ~/.zshrc

```
