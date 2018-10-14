> Login

```bash
git config --global user.name "username"
git config --global email.name "email"
```

> 初始化一个Git仓库

```bash
git init
```

```bash
//GitHub创建库后clone
git clone <URL>
```
> 添加文件到Git仓库

```bash
//可以用git add .直接将所有文件放入暂存区
git add <file>

//提交到版本库, 描述本次提交的说明
git commit -m "本次提交的说明"
```

> 获取工作区的状态

```bash
//查看是否有文件进行修改
git status

//查看修改内容
git diff
```

> 版本控制

```bash
//查看提交日志
git log
//HEAD代表当前版本, HEAD^是上个版本, HEAD^^上上个版本, HEAD~N前N个版本
//也可以用版本号指定

git reset --hard <version>
//由于使用reset回退版本后之前版本的提交日志也会消失
//可以显示你每次命令可以查看到被你回退的版本号
git reflog
```

> 撤销修改

```bash
//让文件回到最近一次git add或者git commit的状态
git checkout -- <file>

//将文件移出暂存区, 即取消git add操作
git reset HEAD -- <file>
```

> 删除文件

```bash
//与git add的用法一样
//从版本库里中删除文件
git rm <file>
git commit -m "本次提交的说明"
```
