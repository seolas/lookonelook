### 问题描述

```console
Julia@DESKTOP-H7U5YL8 MINGW64 ~
$ git clone git@github.com:seolas/atcrowdfunding-parent.git
Cloning into 'atcrowdfunding-parent'...
ssh: connect to host github.com port 22: Connection timed out
fatal: Could not read from remote repository.
```

### 解决方案

```console
Julia@DESKTOP-HJ4UV7L MINGW64 ~
$ cd .ssh
$ touch config
$ vim config

# 添加到 config 文件中
Host github.com
  User "onlyrowoon@gmail.com"
  HostName ssh.github.com
  PreferredAuthentications publickey
  IdentityFile ~/.ssh/id_rsa
  Port 443
```

### 参考链接

[【Git】ssh: connect to host github. com port 22: Connection timed out 的解决方案](https://blog.csdn.net/MBuger/article/details/70226712)
[Solution for 'ssh: connect to host github.com port 22: Connection timed out' error ](https://gist.github.com/Tamal/1cc77f88ef3e900aeae65f0e5e504794)
