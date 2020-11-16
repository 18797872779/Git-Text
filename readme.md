
# GIT使用

工作区 - 暂存区 - 本地仓库

1. 在电脑上创建一个文件夹作为工作区
2. 打开文件夹右键 git base here 进入当前目录
3. 工作区持有项目实际文件
4. 暂存区和本地仓库 不需要我们操作！！

## readme 文档
1. readme文件可以txt文档，也可以是md文档
2. 一般和项目放在一起，作为项目的说明文档

## 全局配置
1. 配置用户名：git config --global user.name "你的git名称"
2. 配置用户邮箱：git config --global user.email "你的git验证邮箱"
3. 一台电脑配置一次就可以了
4. 查看你的配置信息：git config --list

## 初始化
1. 命令 git init 初始化版本库
2. 当前目录路径后面有(master)代表初始化成功
3. 在当前目录下会生成一个隐藏文件 .git 代表这是一个版本库
4. 千万别操作 .git 文件，让他隐藏不管它

## 工作区内容提交到本地仓库
1. 执行命令 git add 文件名 将工作区的内容提交到暂存区
2. 命令 git add . 将所有变动（新增、修改、删除）提交到暂存区
3. 从暂存区提交到本地仓库 git commit -m '提交注释'

## 版本回退
1. 命令：git reset --hard HEAD^  回退到上一个版本（一个^代表上一个版本）
2. 命令：git reset --hard 版本号  回退到指定版本

## 辅助命令
1. 命令 git status 查看当前目录下的操作状态
2. git log 查看日志
3. git reflog 查看简版日志

## 将本地仓库提交到远程仓库
1. 在github创建一个远程仓库 Git-Text
2. 本地工作区先提交到本地仓库
3. git remote add origin 远程仓库地址  本地仓库和远程仓库关联
4. git remote -v  查看本地仓库所关联的远程仓库地址
5. git push -u origin master  第一次执行
  git push 把本地仓库推送到远程仓库
  -u origin master 设置默认提交master分支到origin
6. git push -u -f origin master 强制推送到远程，不推荐！！



## 下载项目到本地
1. 克隆项目：git clone 项目远程仓库地址，整个版本克隆下来
2. git clone 适用于本地没有该项目，直接从远程下载到本地
3. 一定要先把工作区的修改提交到本地仓库再更新远程到本地
4. 如果本地有该项目 ，应该直接更新到本地 ：get pull
5. git fetch 将远程更新到本地



## 分支操作
1. 查看当前仓库的所有分支 ：git branch，查看远程仓库分支： git branch -r
2. 当前分支前面都带有星号*
3. 创建分支：git branch 分支名
4. 切换到哪个分支：git checkout 分支名  
5. 切换分支之后，工作区的代码自动切换到对应分支的代码
6. 合并分支：git merge test 把test分支合并到当前分支
7. 删除分支 ：git branch -D 分支名
8. get pull origin dev 更新代码到本地，自动合并到当前分支，没有记录
9. get fetch origin dev 更新代码到本地，不会自动合并到当前分支
10. git merge FETCH_HEAD ：合并代码到当前分支


## 添加协作者
1. 在当前项目位置 点击 setting


## 配合ssh秘钥
1. 生成秘钥：
2. 找到
3. 拖到
4. github
5. 选择
6. new
7. 粘贴
8. 点击
9. 本地


## git忽略列表
1. 创建文件：.gitignore
2. 忽略文件列表
3. 在忽略列表中列出