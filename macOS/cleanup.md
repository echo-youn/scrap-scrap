# 클린 설치 후 세팅

## Homebrew
설치
```
-- Xcode 이때 설치 됨.
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

brew update

/****************** Dev Tools ********************/

brew install git iterm2 docker docker-compose node vnm curl maven gradle

brew install --cask google-chrome slack postman dbeaver-community intellij-idea visual-studio-code github 

brew tap AdoptOpenJDK/openjdk

brew install --cask adoptopenjdk8 adoptopenjdk11

/************* 단축어 *************/
echo "alias ll='ls -al'" > ~/.zshrc

```
