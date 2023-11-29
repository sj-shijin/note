## 0.Github连接问题

### 修改hosts文件

1. 文件地址

   [`C:\Windows\System32\drivers\etc\hosts`](C:\Windows\System32\drivers\etc\)

2. 添加内容（内容会改变）

   ```
   140.82.113.3 github.com
   199.232.69.194 github.global.ssl.fastly.net
   185.199.108.153 assets-cdn.github.com
   185.199.109.153 assets-cdn.github.com
   185.199.110.153 assets-cdn.github.com
   185.199.111.153 assets-cdn.github.com
   ```

3. 内容获取

   Line1：[Github网址IP地址](https://github.com.ipaddress.com/)

   Line2：[Github域名IP地址](https://fastly.net.ipaddress.com/github.global.ssl.fastly.net)

   Line3-5：[Github静态资源IP地址](https://github.com.ipaddress.com/assets-cdn.github.com)

### 刷新DNS缓存

在cmd中执行`ipconfig/flushdns`命令

## 1.基本信息

**Git**分为远程仓库、本地仓库（暂存区）、工作区

![img](Git.assets/git-command.jpg)

- 远程仓库：储存在云端，一般用于与他人共享。
- 本地仓库：储存在本地的项目文件夹`.git`
  - 暂存区：一般存放在`.git/index`中
- 工作区：通过vscode等软件中打开的文件

## 2.常用命令

通过**GitBash**命令行打开当前文件夹。

```
# 初始化
git init
# 从远程仓库下载一个项目到本地仓库
git clone ‘远程仓库地址’
# 将工作区的文件添加到暂存区
git add .(所有文件)/文件名
# 比较工作区与暂存区的文件差异
git diff
# 将暂存区的内容添加到本地仓库
git commit -m [备注信息]
# 将本地仓库的文件上传到远程仓库
git push ‘远程仓库地址’
# c
git pull ‘远程仓库地址’
```





