### 1. 在Ubuntu软件商店下载时报错Code：409
* 解决方法：在命令行中输入：
    
    ` snap changes`检查状态
    
    `snap abort ID `强制关闭即可
### 2. 下载软件时被中止后报错显示等待缓存锁
* 第一种方法强制解锁命令：
```` 
rm /var/lib/dpkg/lock-frontend
rm /var/cache/apt/archives/lock
rm /var/lib/dpkg/lock 
````
* 第二种方法：

终端输入 ps aux ，列出进程。找到含有apt-get的进程，直接sudo kill PID。（暂时没使用）
### 3.在Ubuntu中软件商店下载vscode后不能输入中文
* 第一种：在官网中下载，但是速度比较慢
* 第二种：命令行下载

    更新软件包索引并安装依赖软件` sudo apt install software-properties-common apt-transport-https wget`

    插入Microsoft GPG key` wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add - `

    启动vscode源仓库` sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"`

    apt软件源被启动，安装vscode软件包` sudo apt install code`

### 4.官网下载安装qq音乐后无法打开的问题
````
cd /usr/bin/
ls
ls |grep qqmusic
pwd
sudo vim /usr/share/applications/qqmusic.desktop
apt install vim
sudo vim /usr/share/applications/qqmusic.desktop
sudo chmod +x music
cat /usr/bin/music
/usr/bin/qqmusic --no-sandbox
````

