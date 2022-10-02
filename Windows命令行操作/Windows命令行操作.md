# Windows命令行操作

### 1.常用命令

#### （1）cd命令

```Dos
#进入某个盘，盘符+:
D:
#跳转到硬盘的根目录
cd \
#跳转到当前目录的父目录
cd ..
#跳转到当前目录下硬盘的其他文件地址处
cd C:\yjlpku
#跳转到其他硬盘的文件夹处
cd /d E:\Typroa
```

#### （2）查看目录下的文件

```Dos
dir
#和Linux中的ls命令作用相同
```

#### （3）创建和删除目录

```Dos
#创建目录
md 目录名(文件夹)
#删除目录
rd目录名(文件夹)
#特别的有一个命令用来删除文件
del 目录下文件名
```

#### （4）文件拷贝和移动

```Dos
move 路径\文件名 路径\文件名
#把一个文件移动到另一个地方

copy 路径\文件名 路径\文件名
#把一个文件拷贝到另一个地方
```

#### （5）其他命令

```Dos
cls
#清空命令行

ipconfig
#查看本机ip
```

### 2.查看cmd下的命令

#### （1）帮助指令

```Dos
命令 -help 或者 命令 /？
#都可以查看命令的属性
```

### 3.Windows快捷键

```Windows
win+E
#打开文件资源管理器

win+D
#显示桌面

win+L
#锁定桌面

Alt+F4
#关闭当前程序

Ctrl+Shift+Esc
#打开任务管理器
```

![DOS命令(1)](E:\CS自学\Tool\Git\Windows命令行操作\DOS命令(1).png)

<img src="E:\CS自学\Tool\Git\Windows命令行操作\DOS命令(2).png" style="zoom:130%;" />