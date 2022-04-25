# 1 

…or create a new repository on the command line
echo "# test" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/fcqfcq/test.git
git push -u origin main


…or push an existing repository from the command line
git remote add origin https://github.com/fcqfcq/test.git

git branch -M main
git push -u origin main
…or import code from another repository


git config --global user.email "18071458891@163.com"
git config --global user.name "fcqfcq"

# 2
提交第一行代码
git commit
在创建完仓库之后，用户可以通过如下方式，可以向仓库提交第一行代码。

此处我们以用户账号下命名为 HelloGitee 的仓库为例。对应的仓库地址为：https://gitee.com/用户个性地址/HelloGitee.git，在实际实践中，你可以将用户个性地址替换为自己的地址。

方法1、先将仓库clone到本地，修改后再push到 Gitee 的仓库
$ git clone https://gitee.com/用户个性地址/HelloGitee.git #将远程仓库克隆到本地
在克隆过程中，如果仓库是一个私有仓库，将会要求用户输入 Gitee 的账号和密码。按照提示输入即可。

当然，用户也可以通过配置本地的git配置信息，执行git config命令预先配置好相关的用户信息，配置执行如下：

$ git config --global user.name "你的名字或昵称"
$ git config --global user.email "你的邮箱"
在 Gitee 平台中，强烈建议您在【设置-多邮箱管理】中的“提交邮箱”与上面配置信息中的邮箱地址保持一致，这样平台就能及时地统计您在平台中提交代码的贡献了。

修改代码后，在仓库目录下执行下面命令

$ git add . #将当前目录所有文件添加到git暂存区, 文件添加到 暂存区
$ git commit -m "my first commit" #提交并备注提交信息 ，提交到本地仓库
$ git push origin master #将本地提交推送到远程仓库 ，推送到远程仓库
方法2、本地初始化一个仓库，设置远程仓库地址后再做push 
和方法1的差别，在于先创建仓库。

$ git init 
$ git remote add origin https://gitee.com/用户个性地址/HelloGitee.git # 远程创建仓库
这样就完成了版本的一次初始化。
接下去，进入你已经初始化好的或者克隆仓库的目录,然后执行：

$ git pull origin master
修改/添加文件，否则与原文件相比就没有变动。

$ git add .
$ git commit -m "第一次提交"
$ git push origin master
然后如果需要账号密码的话就输入账号密码，这样就完成了一次提交。此时，你可以在你的个人面板、仓库主页查看到你的提交记录。

在新建仓库时，如果在 Gitee 平台仓库上已经存在 readme 或其他文件，在提交时可能会存在冲突，这时用户需要选择的是保留线上的文件或者舍弃线上的文件，如果您舍弃线上的文件，则在推送时选择强制推送，强制推送需要执行下面的命令(默认不推荐该行为)：

$ git push origin master -f
如果您选择保留线上的 readme 文件,则需要先执行：

$ git pull origin master