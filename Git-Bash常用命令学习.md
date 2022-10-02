# Git-Bash  常用命令学习

## 工作路径和文件操作

- ls

```Linux
ls
#查看当前目录下的文件
ls -l
#显示文件的详细信息
ls -a
#列出所有的文件夹
ls -A
#列出除了.和..的文件
ll
#显示的内容更加详细
```

- cd 和 pwd

```Linux
cd ~
#进入家目录
cd -
#进入上一次工作路径
cd 工作路径 E:/CS自学/Programme/CS61A
#使用反斜杠
pwd
#返回当前工作路径
```

- mkdir 和rmdir、rm、touch

```Linux
mkdir <name>
#在当前工作目录下创建一个名为<name>的文件夹
mkdir -p 文件夹名称
#可以在工作环境下创建一个文件夹里面的子文件夹
rm -r
#删除某个文件夹，同时删除目录；删除某个文件
touch 
#新建一个文件，需要输入文件后缀名
```

- mv 和 cp

```Linux
mv 文件地址 新文件地址

```

- clear 和reset

```Linux
clear
#清屏
reset
#重新初始化终端、清屏
```

