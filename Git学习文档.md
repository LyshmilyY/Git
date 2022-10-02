# Git

# Git管理系统有三个区域，暂存区、本地库和远程库

## Git操作指令合集

<img src="E:\CS自学\Tool\Git\Git操作指令.png" alt="Git操作指令" style="zoom:150%;" />

## 1.基本操作

#### （1）git init ——初始化仓库



```git
$mkdir git-tutorial
#新建一个名为git-tutorial的文件夹
$cd git-tutorial
#将git-tutorial作为工作目录

$git init
#初始化本地仓库
#初始化后，文件夹里会出现一个.git文件夹，这个目录下存储着管理当前内容所需要的仓库数据
```

#### （2）git status——查看仓库的状态

```git
$git status
#返回包括仓库处于哪个分支下以及需要提交的内容，“提交”指的是“记录工作树中所有文件的当前状态”
```



#### （3）git add——向暂存区中添加文件

```git
$git add
#仓库里的文件一开始并没有在Git仓库的版本管理对象中，如果我们新建文件也不会出现在Git的版本管理中，当我们使用git status查看时，存在的文件都会显示在Untracked files里，使用git add会将文件添加在暂存区。

$git rm --cached <file>
#将某个文件停止追踪，移出Git版本管理对象，仅限于对暂存区的文件。
```



#### （4）git commit——保存仓库的历史记录

```git
$git commit -m"提交信息"
#将暂存区的文件保存到本地库，并且提供一个对于文件的描述，类似于第几次修改；关于什么类型的文件，有点像文件的标签。
#如果没有-m，我们将会得要详细说明更改内容、更改原因和详细内容。
```

#### （5）git log——查看提交日志

```  git
$git log 
#可以得到最近的一次commit，得到结果commit的哈希值表示、commit的Author的名字和邮箱、日期和标签。

$git log --pretty=short
#可以显示简短的提交信息

$git log <file>
#只显示指定目录或文件的日志

$git log -p
#显示文件更改前后的差别

$git log -p <file>
#显示某个文件或者目录下的日志和提交前后的差异
```

#### （6）git diff——产看更改前后的差别

```git
$git diff HEAD
#本次提交和上次提交之间的区别
```

## 2.分支的操作

在进行多个并行作业时，我们会用到分支，例如我们创建多个分支。

#### （1）git branch——显示分支一览表

```git
$git branch
#显示分支一览表
#当前所在分支前面会有一个*号
$git branch <name>
#创建一个名为<name>的分支，但是没有切换分支
```

#### （2）git checkout -b——创建、切换分支

```git
$git checkout-b <name>
#创建一个名为<name>的分支，并且将当前分支切换到<name>分支

#这个操作等价于下面的这两行代码
$git branch <name>
$git checkout <name>
```

#### (3) git merge——合并分支

```git
$git merge --no-off <name>
#将分支<name>合并到主分支master，并且创建合并信息commit
```

#### （4）git log --graph——以图表形式查看分支

```git
$git log --graph
#能够以图标的形式显示出特性分支和主分支以及修改合并的操作
```

## 3.更改提交的操作

#### （1）git reset——回溯历史版本

```git
$git reset --hard
#哈希值
#我们输入一个哈希值后可以回溯到之前的某一个状态

$git reflog 
#查看当前仓库执行过的操作日志
```

#### （2）git commit --amend——修改提交信息

```git
$git commit --amend
#修改上一条提交的信息，修改commit内容
```

#### （3）git rebase -i——压缩历史

```git
$git rebase -i HEAD~<number>
#将最新提交的commit合并为一个commit
```

## 4.推送至远程库

#### （1）git remote add——添加远程仓库

```git
$git remote add <name> https:/github.com
#我们将远程仓库https:/github.com设置为本地库的远程仓库，并将这个仓库的别名设为<name>
```

#### （2）git push——推送至远程仓库

```git
$git push -u <name> <branch name>
#将<branch name>分支内容推送到远程仓库，必须保证本地库和远程仓库内容相同，不相同要先拉取。
```

## 5.从远程库获取

#### （1）git clone——获取远程仓库

```git
$git clone https:/github.com
#将GitHub上的仓库clone到本地，不能和之前的仓库在同一目录下
```

#### （2）git pull——获取最新的远程仓库分支

```git
$git pull <仓库> <branch name>
#获取远程仓库的分支最新内容到本地库
```





