## 什么是`git`？
`git`就是分布式版本控制系统，一种用来协助开发的工具。
`git`有许多功能：
版本回退；
推送到远程仓库（如`github`)；
拉取远程仓库的内容；
...
## 安装`git`
点击[官网下载链接](https://git-scm.com/downloads/win)
选一个你喜欢的安装位置
把这个勾上，将`git`添加到终端
![](https://img2024.cnblogs.com/blog/3460892/202505/3460892-20250531175229366-1584005902.png)
其余的选择默认即可
这样就下载完成了，右击桌面打开终端，就可以看到Git Bash的终端选项
![](https://img2024.cnblogs.com/blog/3460892/202505/3460892-20250531175535479-827963880.png)
![](https://img2024.cnblogs.com/blog/3460892/202505/3460892-20250531175605748-633704456.png)
你可以在`PowerShell`或者`Git Bash`中输入`git --version`显示git版本号来验证是否下载成功
![](https://img2024.cnblogs.com/blog/3460892/202505/3460892-20250531180204546-269743915.png)
![](https://img2024.cnblogs.com/blog/3460892/202505/3460892-20250531180212228-354892245.png)



## 使用`git`
前面说到git可以帮助我们拉取和推送远程仓库的内容，现在我们一步步操作一下。
1. 自行注册好`github`账号
2. 将`github`账号信息添加到全局`git`中（username、useremail）
在`powershell`或者`gitbash`中使用下面两条命令
![](https://img2024.cnblogs.com/blog/3460892/202505/3460892-20250531181009677-1029650974.png)
将引号内的`name`和`email`换成你注册`github`使用的`name`和`email`
3. 下面将测试一下将本地的代码推送到远程仓库
- 在一个你喜欢的地方创建一个项目文件夹`Demo`，不要像我一样把项目文件夹放在C盘下，因为我在虚拟机下没有将磁盘进行分区
![](https://img2024.cnblogs.com/blog/3460892/202505/3460892-20250531181515569-801384612.png)
- 随便在Demo下放一些文件
![](https://img2024.cnblogs.com/blog/3460892/202505/3460892-20250531181901049-1988366319.png)
如果你没用过`vim`,请不要执行`vim t1.txt`
然后我们将`Demo`这个文件夹推送到github中
4. 推送
首先我们在`github`中创建一个`Demo`仓库
![](https://img2024.cnblogs.com/blog/3460892/202505/3460892-20250531182359851-851126009.png)
创建好后复制https链接或者ssh密钥
https例如`https://github.com/Thintime123/Demo.git`
shh（需要另外配置）例如`git@github.com:Thintime123/Demo.git`
下面以https示例
在终端使用（`Demo`目录下）
`git init`
`git remote add origin https://github.com/Thintime123/Demo.git`添加远程仓库
使用`git status`查看git变更
使用`git add .`将所有变更添加到缓存区
使用`git commit -m "commit message`提交
初次推送`git push -u origin master`
以后`git push`这会推送到默认分支
推送其他分支`git push origin branch_name`
![](https://img2024.cnblogs.com/blog/3460892/202505/3460892-20250531183815031-795770422.png)
推送成功，我们在github中查看一下
![](https://img2024.cnblogs.com/blog/3460892/202505/3460892-20250531183849303-1838262492.png)
5. 拉取操作
在其他开发者推送了代码之后我们想拉取最新提交时，只需要执行如下操作
`git pull origin master`
将`master`替换成需要拉取的分支，如果的默认分支可以直接`git pull`
比如我们在github中Add Readme之后
![](https://img2024.cnblogs.com/blog/3460892/202505/3460892-20250531184156397-1284665163.png)
![](https://img2024.cnblogs.com/blog/3460892/202505/3460892-20250531184224959-299590777.png)
可以看到README.md已经拉取到本地仓库了
6. 好了，现在你已经学会了git的最常见的操作，git还有很多很多用法，大家会在后续的使用中慢慢接触到的

