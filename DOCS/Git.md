#Git 学习笔记（一）
这个月以来，大部分时间是在总结和思考之前学过的东西。而Github的使用学习，让我获得了一种更高效的学习方式：先把代码敲过一遍，实现了相应的效果，即使不理解，这样对于眼前的代码也能有一个感性的认识，之后再针对性寻找不明白的地方的相关文档阅读，比起之前拿起一本书就开啃，从头扫到尾的方式，这样可以节省很多时间。而贯穿其中的同时也是我觉得最重要的就是——做笔记，一开始的笔记肯定是很乱的，而后来的整理至关重要，这一步对于形成系统的知识必不可少。之前的学习也因为少了这一步，导致效率一直不高。

好了，些许感悟不值一提。接下来感性认识一下Git，直接操作起来。注：但凡代码中出现"laijbin"和"laijbn-notes",将其修改为你自己的用户名和项目名称即可。

## 操作练习（一）：

从零开始，到从本地编辑并推送项目到Github的操作。

1.  创建Github账号，上[Github官网][1]注册。

2.  下载并安装Git，详细:[安装Git][2]，秘诀就是一路“next”，安装完成后到开始菜单找到Git Bash，点击启动。

3.  设置ssh，建立本地与Github的连接
    
    3.1 运行命令 `$ cd ~/.ssh` 检查自己电脑是否有ssh keys存在，若显示No such file则需新建一个ssh keys； 3.2 新建ssh keys：运行命令 `$ ssh-keygen -t rsa -C "youremail"` 回车，然后输入你的密码，并再次输入确认。注意输入密码时虽然看不到，但已经输入点击回车即可。 3.3 到代码显示的文件夹中找到你的密匙文件id_rsa.pub，如： C:/Users/用户名/.ssh/文件夹中。用记事本打开文件，复制全部内容。到Github网站，找到"Account settings"点击——>"SSH Keys" 点击——>"Add SSH key"。把复制内容粘贴进去，"Title"一栏内容随便填。 3.4 检验

4.  在GIthub网站上新建一个仓库，比如名字为"laijbin-notes";

5.  本地配置Git，输入命令：

> `$ git config --global user.name "yourname"`
> 
> `$ git config --global user.email "youremail"`

这两步所添加的信息可用 `$ cat ~/.gitconfig` 命令查看到

<pre>6. 本地新建仓库，注意要和Github上的项目名称相同。执行以下命令： 
</pre>

> `$ mkdir laijbin-notes` #新建项目
> 
> `$ cd laijbin-notes\` #进入文件
> 
> `$ git init` #初始化，本地出现项目文件
> 
> `$ touch README` #新建README文件
> 
> `$ echo "Hello beauty" >> README` #在README里写入"Hello beauty"
> 
> `$ git add README` #跟踪README文件，把README放到暂存区
> 
> `$ git commit -m '1st'` #将修改提交到本地仓库
> 
> `$ git remote add origin git@github.com:laijbin/laijbin-notes.git` #添加远程仓库
> 
> `$ git push -u origin master` #将本地修改推送到远程仓库

完成操作到Github刷新你的仓库，会神奇的发现有"laijbn-notes"仓库里含有内容为"Hello beauty"的README文件了，没错，这一切都是你干的。



 [1]: http://github.com/
 [2]: http://gitbook.liuhui998.com/2_1.html/