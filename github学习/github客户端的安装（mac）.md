#github客户端的安装（mac） 


#####客户端的下载及注册账
下载安装git客户端 http://code.google.com/p/git-osx-installer/downloads/list?can=3

注册github账号 https://github.com/ -->Pricing and Signup -->Create a free account 

#####创建ssh：   
接下来打开终端(不知道终端在哪儿的，就直接在spotlight里搜terminal)：

    $cd ～/.ssh  //检查是否已经存在ssh
    
如果存在，先将已有的ssh备份，或者将新建的ssh生成到另外的目录下，如果不存在，通过默认的参数直接生成ssh:

    $ssh-keygen -t rsa -C xxxxx@gmail.com（注册github时的email）
        Generating public/private rsa key pair.
        Enter file in which to save the key (/Users/twer/.ssh/id_rsa): 
        Created directory '/Users/twer/.ssh'.
        Enter passphrase (empty for no passphrase): 
        Enter same passphrase again: 
        Your identification has been saved in /Users/twer/.ssh/id_rsa.
        Your public key has been saved in /Users/twer/.ssh/id_rsa.pub.
        The key fingerprint is:
        18:16:11:c9:01:6c:48:09:7f:27:c6:43:0d:7f:3f:84 xxxxx@gmail.com
        The key's randomart image is:
        +--[ RSA 2048]----+
        |.o.++===         |
        |.ooo.+. .       |
        |  ..* = E .      |
        |   o = + o       |
        |      . S o      |
        |           .     |
        |                 |
        |                 |
        |                 |
       +-----------------+

在github中添加ssh：

这步比较崩溃，找不到文件。。**直接在terminal里打：vim ~/.ssh/id_rsa.pub**


       登陆github，选择Account Settings-->SSH  Keys 添加ssh
       Title：xxxxx@gmail.com
       Key：打开你生成的id_rsa.pub文件，将其中内容拷贝至此。

打开终端，先测试一下你的帐号跟github连上没有：ssh -T git@github.com 
如果出现如下提示，表示你连已经连上了.(因为有了第一步,
所以不用自己做过多的连接github的操作了，另外，下一次要连接github的时候记得打开第一步的工具).

    Hi MiracleHe! You've successfully authenticated, but GitHub does not provide shell access.
