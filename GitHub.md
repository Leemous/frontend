### 如何配置GitHub本地仓库
1. 首先，你需要创建一个文件夹（这不废话么）
2. 下面进入命令行模式（因为客户端管理工具我琢磨了一个小时无果），其实命令行也没有那么难啦！
3. 为了节省更多时间用于学习，我们简化一下文件管理的操作，只在一开始进行比较复杂的配置
4. 下面跟我一步步配置学习环境吧～

##### 配置SSH秘钥
1. 首先我们看一下机器上是有已经有了SSH秘钥，打开终端，输入命令：
  <pre>
    $ cd ~/.ssh
    $ ls
  </pre>
2. 如果能看到id_rsa文件（通常认为是默认的ssh文件），说明设备上已有ssh的配置，如果没有，我们生成一个。
3. 生成SSH的命令如下：
  <pre>
  $ssh-keygen -t rsa -C "email@email.com"
  </pre>
  紧接着出现提示：

  > Enter file in which to save the key (/Users/{userName}/.ssh/id_rsa):

  这个是让你输入存储ssh秘钥的文件名，我们是用于github网站的，建议用id_rsa_github标识。

  输入文件名后回车，然后会出现提示：键入密码，直接回车带过即可（即默认没有密码，如果键入了密码，之后提交代码时都需要输入密码），然后是确认密码，直接回车。<font color=red>注意命令是区分大小写的～</font>

  成功生成后，再次键入命令：
  <pre>
    $ ls
  </pre>
  发现多出来了两个文件：id_rsa_github和id_rsa_github.pub，前者是<font color=#FF8247>私钥</font>，任何情况不能提供给别人的，后者是<font color=#00F5FF>公钥</font>，需要添加到github后台设置中去，也就是把<font color=#00F5FF>公钥</font>给我啦！

  给我的公钥内容，输入命令查看：
  <pre>
  $cat id_rsa_github.pub
  </pre>

  可以看到一串字符，从ssh-rsa开始复制到邮箱结束即可。
  最后一步：把<font color=#FF8247>私钥</font>添加到钥匙串中，输入命令：
  <pre>
  $ssh-add id_rsa_github
  </pre>
  至此我们就完成SSH的生成与配置了。

##### 初始化本地GitHub仓库

  1. 打开终端，进入你创建的本地仓库文件夹，以路径/user/leemaz/learning/为例

  输入命令：
  <pre>
  $ cd ~/learning
  </pre>
  <font color=red>想确定是否进入文件夹？看命令行前缀，设备名后面紧跟着的是你当前所处的文件夹位置，如果显示Air:learning代表成功进入文件夹</font>

  2. 输入命令：
  <pre>
  $ git init
  $ git config user.name "GitHubUsername"
  $ git config user.email "GitHubEmail@email.com"
  </pre>

  上面几条命令完成了以下工作：

  **初始化了本地仓库，把learning作为一个github本地仓库根目录，我们为它配置了用户名及邮箱，作为提交（Commit）时所有人可见的标识**

  现在你可以克隆远程仓库代码到本地了。

##### 克隆远程仓库代码到本地
1. 远程仓库url的获取

  在GitHub仓库主界面中，有一个醒目的按钮：<font color=#28a745>Clone or download</font>，点击它会弹出小盒子，右上角如果是Use SSH，则点击，否则直接复制输入框中的url
2. 打开终端，进入本地仓库文件夹

  记得命令吗？是这个样子的：
  <pre>
  $ cd ~/learning
  </pre>
  然后输入克隆的命令：
  <pre>
  $ git clone "remote-repository-url"
  </pre>
  出现以下提示，代表成功克隆了远程仓库代码到本地：

  > Receiving objects: 100% (10/10), done.

  括号里的数字代表：**克隆成功文件数/目标文件数**
##### GitHub提交操作
