### 配置Atom
##### 下载与安装
地址：https://atom.io/
##### 安装插件
1. open-in-browser
  插件的作用：右键文件、编辑器面板时，会有一个"Open In Browser"的选项，不需在浏览器输入路径去访问本地文件啦～

  > 打开：Packages-SettingView-Install Packages/Themes

  > 输入：open-in-browser

  > 安装搜索结果第一位的包，点击Install等待安装完成即可

  > 我安装比较顺利，所以如果你的安装出现问题，我们再一起解决

2. Emmet

  Emmet是一款非常强大的HTML/CSS代码快速编写神器，可以帮助你快速书写HTML页面，它不是必备的，但有了它是可以做到事半功倍的。

  > 打开：Packages-SettingView-Install Packages/Themes

  > 输入：Emmet

  > 安装搜索结果第一位的包，点击Install等待安装完成即可

  > 安装失败时，可以打开代理重试

3. GitPlus

  安装了这个插件，我们就不用在Atom与终端之间切换了，可以直接在Atom中输入git命令

  > 打开：Packages-SettingView-Install Packages/Themes

  > 输入：git-plus

  > 安装搜索结果第一位的包，点击Install等待安装完成即可

  Git提交有几个重要的步骤：
  1. 获取远程仓库最新代码到本地仓库；
  2. 将你当前文件系统中的代码与本地仓库代码做比对，有冲突则需要解决冲突；
  3. 对比并解决完冲突后，添加所有的更改到本地仓库；
  4. 提交当前的更改，需要输入变更提交信息；
  5. 将本次更改提交到远程仓库。

  合并到Atom的操作即为：
  1. 文件（夹）右键-Git-Git pull，完成上述步骤1、2的操作（解决冲突可能需要手动，遇到了再补充）；
  2. 文件（夹）右键-Git-Git add+commit，完成上述步骤3、4的操作（此时会弹出一个输入提交信息的区域，填写一些文件描述后保存即可）；
  3. 文件（夹）右键-Git-Git push，完成上述步骤5的操作。

  其实还有更牛逼的方法：

  Atom-Packages-Git Plus-Add(All)+Commit+Push，直接完成全部操作，但只适合新文件的提交，前提能够确保不会产生冲突，强烈建议在GitPlus的Setting中勾选"Pull Before Pushing"，它会对远程仓库文件起到一定的保护作用。

100. Atom插件推荐：http://blog.csdn.net/zsl10/article/details/51822715
