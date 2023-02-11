### 1. inputting method Setting切换输入法
* `apt remove ibus`删掉ibus输入法
* `apt install fcitx-bin fcitx-table`下载google输入法
* `im-config`设置google输入法

### 2.下载Google Chrome游览器 
* 官网下载相应打deb包
* 解压安装`sudo dpkg -i google-chrome-stable_current_amd64.deb`
* To：安装完后在设置中找到语言进行相应的更新

### 3.下载播放器vlc
* `sudo apt install vlc`

### 4.安装QQ(Tim)以及其他软件
* 这里简单把qq单独列出来讲是因为Linux原生qq界面真的丑，和上一代老人机页面有得一拼。网上较好的处理方法是下载星火软件商店，并且确实很好用，网上主流的软件也几乎都有，比如qq、微信（优麒麟下载的）、迅雷、Tim、网易云音乐、qq音乐等。
* 下载方法：官网：https://www.spark-app.store/download
    1. 如果是Ubuntu22.04版本，可直接下载软件本体，并使用他推荐的命令：sudo apt install ./spark-store_3.2.3_amd64.deb(使用dpkg的命令会出现问题，可能也是每个主机不一样导致的，看到别人的可以使用)
    2. Ubuntu其他版本使用依赖包，按照里面的说明进行安装
    3. 安装完成后打开软件商店便可以直接下载软件啦，尽量找不是Wine的吧
    4. 如果有下到不需要的安装包，不用管他，因为在电脑下次重新启动时会自动删除。

### 5.安装OBS studio
* 为什么要把这个拿出来单独讲呢？
    1. 首先，OBS它是有原生的Linux安装包的，加上Ubuntu商店支持的OBS并没有中文显示，所以还是劝退。
    2. 下载官网：https://obsproject.com/wiki/install-instructions#linux
    3. 使用命令:
        * sudo add-apt-repository ppa:obsproject/obs-studio
        * sudo apt update
        * sudo apt install obs-studio
    4. 当然如果想要使用虚拟摄像头，需要下载其他的包，至少官网是有说明。
    5. 在使用`sudo apt install v4l2loopback-dkms`命令时最好是关闭BIOS里面的Secure boot，将其设置为disenable。

### 6.安装微信
* 第一种微信是从优麒麟下载的，当然如果你安装了星火软件商店，那么更推荐你使用软件商店。
* 第二种下载操作：
    1. 首先下载包（点击网址下载即可）：http://archive.ubuntukylin.com/software/pool/partner/ukylin-wine_70.6.3.25_amd64.deb
    2. 第二个包：http://archive.ubuntukylin.com/software/pool/partner/ukylin-wechat_3.0.0_amd64.deb
    3. 命令：
        * `sudo apt-get install -f -y ./ukylin-wine_70.6.3.25_amd64.deb`
        * `sudo apt-get install -f -y ./ukylin-wechat_3.0.0_amd64.deb`
    4. 第二种不太推荐，容易报错

### 7.卸载软件命令：
* 删除软件及其配置文件：`sudo apt-get --purge remove 软件名`
* 只删除软件：`sudo apt-get remove 软件名`

### 8.为Ubuntu Dock图标启用最小化单击功能（minimize on click）
* 命令：`gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'minimize'`

### 9.为Ubuntu下载Cleaner
* 命令：
    ````
    sudo add-apt-repository ppa:gerardpuig/ppa
    sudo apt-get update
    sudo apt-get install ubuntu-cleaner
    ````



