#Git 学习笔记
1. 创建Github账号，上[Github官网](http://github.com/)
2. 下载并安装Git，详细:[安装Git](http://gitbook.liuhui998.com/2_1.html/)，安装完成后到开始菜单找到Git Bash，点击启动。
3. 设置ssh，建立本地与Github的连接
>   3.1 运行命令$ cd ~/.ssh检查自己电脑是否有ssh keys存在，若显示No such file则需新建一个ssh keys；
>   3.2 新建ssh keys：运行命令$ ssh-keygen -t rsa -C "你的邮箱" 回车，然后输入你的密码，并再次输入确认。注意输入密码时虽然看不到，但已经输入。
    3.3 找到
