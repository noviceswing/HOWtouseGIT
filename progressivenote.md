# 常用指令
**准备阶段**
```git init```:将本地目录转换为一个GIT仓库
```git clone + <url>```:克隆一个已经存在的GIT仓库

**使用状态**
```git status```:查看文件状态
```git add .```:将所有更改都加入暂存状态
```git commit -m " 注释 "```:提交所有的更改

**远程仓库的使用**
```git remote add <shortname> <url>```:加入一个远程的仓库（使用于自身有文件，想要和github上的一个仓库合并时）合并后的远程仓库名字为：shortname

```git remote```:查看远程仓库信息
```git fetch <remote>```:从远程仓库进行抓取
```git push <remote> <branch>```:推送到远程仓库

如果使用的是Github此时大概率会出现一个问题，因为GitHub默认主branch为main，但是如果我们直接在文件内```git init```,此时我们的默认分支为master。
解决方法如下：
```git branch -m master main```:将分支master改名为main
```git fetch pb```:获取远程仓库的提交
```git merge --allow-unrelated-histories pb/main```:将远程仓库的提交与自身的提交进行合并
```git push <remote> <branch>```:推送到远程仓库，此时就不会出错了。

### 与github仓库建立连接的正确方式：
在github创建仓库后，在本地文件夹使用git clone指令将远程仓库clone到本地，就不会出现上述的问题了。

