# Clean

## 
```bash
$ sudo apt-get update

$ sudo apt-get install wget gpg git apt-transport-https

$ sudo 
```

## visual studio code
```bash
$ wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg

$ sudo install -D -o root -g root -m 644 packages.microsoft.gpg /etc/apt/keyrings/packages.microsoft.gpg

$ sudo sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list'

$ rm -f packages.microsoft.gpg

$ sudo apt update

$ sudo apt install code
```

## Chrome
```bash
$ wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb

$ sudo dpkg -i google-chrome-stable_current_amd64.deb
```

## Korean Language
```
$ ibus-setup # setup 후 로그아웃
```
