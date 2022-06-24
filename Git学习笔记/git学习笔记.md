# Git学习笔记 --2022/6/24

## 一、Git的初始化配置

```c
/* 1、查看配置 */
$ git config --global --list
/* 2、配置用户名和邮箱（github注册好的） */
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
/* 3、命令行帮助 */
$ git help
/* 4、git ssh配置 */
 ·1.查看是否已经有了ssh密钥：
   	$ cd ~/.ssh
 ·2.生存密钥：
    $ ssh-keygen -t rsa -C “haiyan.xu.vip@gmail.com”

    如果提示 ssh-keygen 不是内部命令或者。。。

    这时候要配置环境变量，具体操作如下：

    1.找到Git/usr/bin目录下的ssh-keygen.exe(如果找不到，可以在计算机全局搜索)

    2.属性-->高级系统设置-->环境变量-->系统变量,找到Path变量，进行编辑，End到最后，输入分号，粘贴复制的		ssh-keygen所在的路径，保存；


    按3个回车，密码为空。

    Your identification has been saved in /home/tekkub/.ssh/id_rsa.
    Your public key has been saved in /home/tekkub/.ssh/id_rsa.pub.
    The key fingerprint is:
    ………………

    最后得到了两个文件：id_rsa和id_rsa.pub

  ·3.添加密钥到ssh：ssh-add 文件名
    $ ssh-agent bash
    $ ssh-add ~/.ssh/id_rsa # 这里如果文件名被改过要写你自己定义的文件名
        
  ·4.在github上添加ssh密钥，这要添加的是“id_rsa.pub”里面的公钥。
    打开https://github.com/ ，登陆账号，然后添加ssh。

  ·5.测试：ssh -T git@github.com
    Are you sure you want to continue connecting (yes/no)?  回答：yes（重要）
    Hi FENG-2020! You've successfully authenticated, bu GitHub does not provide shell 		access.
```

## 二、Git镜像站

- https://hub.おうか.tw
- https://hub.連接.台灣
- https://hub.fastgit.xyz
- https://cdn.githubjs.cf
- https://gitclone.com

## 三、Git命令的使用

* git status 查看状态
* git add 添加文件到暂存区
* git commit -m 更新文件到本地仓库
* git log 查看更新文件到本地仓库的记录
* git push 推送数据
* git pull 拉取数据
* git branch 

