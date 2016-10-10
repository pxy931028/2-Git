### 版本控制工具
+ 分布式：每一台电脑都可以执行提交，查看记录和版本回溯(git)。
+ 集中式：需要中心服务器来处理文件的提交，查看记录，版本回溯等功能(svn)。

### 一、github网站
#### GitHub是一个分布式版本控制与项目托管系统，是一个面向开源及私有软件项目的托管平台，因为只支持 Git 作为唯一的版本库格式进行托管，故名 GitHub。除了 Git 代码仓库托管及基本的 Web 管理界面以外，还提供了订阅、讨论组、文本渲染、在线文件编辑器、协作图谱（报表）、代码片段分享（Gist）等功能。

1.  打开github网址：https://github.com/，登陆github帐号，选择new repository新建一个网络仓库。

2.  管理代码还需要在本地下载一个git工具，用来向github网络仓库管理代码。下载安装git工具后，打开git bash，这时我们需要创建一个本地仓库，创建本地仓库有两种办法：

（1）cd coding：进入coding文件夹。

git init：创建本地仓库，此时coding文件夹就会变成一个本地仓库，会自动生成.git文件。

git remote add origin+网络仓库网址：把本地仓库与网络仓库连接。

（2）git clone+网络仓库网址：把网络仓库克隆到本地。

3.  创建好本地仓库后，在本地仓库新建一个html文件，

git add . :把编辑区文件添加到暂存区。

git commit –m”备注信息”：把暂存区文件添加到主分支。

git push –u origin master:把本地文件提交到网上仓库。

git pull:把网上仓库的内容下载到本地。

### 二、文件状态 常用命令 参数设置
#### 状态：工作区、版本库（暂存区、分支）
#### 常用命令
+ 创建版本库     git init
+ 添加到仓库     git add . (或文件名)  将工作区变动添加到暂存区
+ 提交到仓库     git commit -m "提交说明";  将暂存区内容提交到当前分支
+ 查看状态       git status
+ 查看变动       git diff
+ 查看历史版本号 git log
+ 回溯某个版本   git reset --hard 版本号前六位
+ 回溯上上个版本 git reset --hard HEAD^^
+ 撤销修改       git checkout  --文件名
+ 删除文件       git rm
+ 添加远程库     git push
+ 获取远程库     git pull
+ 查询分支       git branch
+ 创建分支       git branch 分支名称
+ 切换分支       git checkout  分支名称
+ 合并分支       git master
				 git merge
+ 删除分支		 git branch -d 分支名称
+ 删除网上分支   git push -u origin:分支名称
+ 查看远程分支   git remote -v     -v 查看详细信息
+ 创建标签       git tag
+ 帮助文档		 git push --help

### 三、多人协作 解决冲突
原因：两人同时修改同一个文件，其中一个人push，另一个人再push的时候就会出现冲突，可以先pull下来，然后人工解决冲突，然后再push。
