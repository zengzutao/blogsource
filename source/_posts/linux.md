---
title: Linux 常用命令
categories: Linux Commands
author: Jack
tags:
    - Linux
    - Commands
cover_picture: images/linux.jpg
top: 0
---

> _**怅寥廓,问苍茫大地,谁主沉浮?**_ —毛泽东

### 一、路径

1.pwd 显示当前目录

2.cd 改变目录

```bash
cd ~ ：回到主目录
cd - | cd -- ： 跳入上次使用目录
cd .. ：移动到父目录
```

### 二、文件

1. ls 显示所有文件和目录

```bash
ls -l : 显示文件详情
ls -a : 显示所有文件，包括隐藏文件
ls –lH : 以可读格式显示文件
ls –lS : 根据文件大小排序显示
ls –I : 显示inode number  
```

2. touch 创建一个空文件

3. rm 移除文件

4. cp 复制文件

5. mv 移动文件

6. mkdir 创建文件夹

7. rmdir 删除文件夹

8. file 显示文件名和类型

9. chown 改变某个文件或目录的所有者和所属的组

10. chmod命令用来变更文件或目录的权限

11. cat 从头打印显示文件

```bash
cat file1 file2 : 读取多个文件
cat >filename : 创建一个文件并等待用户的输入内容（Ctrl+D结束）
cat file1 > file2 : 将文件 file1 的内容输入到 file2 中
```

### 三、搜索

1. more 向前浏览文件

2. less 向前或向后浏览文件

3. tail 显示尾部的几行

4. head 显示头部几行

5. history 显示所有执行的命令的历史

6. grep 查询字段

7. find 查找文件

### 四、系统

1. ps 显示正在运行的程序

2. kill 结束线程

3. mount 挂载资源

4. umount 移除资源

5. top 查看资源占用情况

### 五、磁盘及网络

1. df 查看磁盘可用容量

2. du 查看磁盘占用情况

3. fdisk 磁盘分区

4. ip 查看当前ip

### 六、用户及用户组

1. useradd 新增用户

2. usermod 修改用户

3. userdel 删除用户

4. passwd 密码相关

5. groupadd 新增用户组

6. groupmod 修改用户组

7. groupdel 删除用户组

### 七、压缩

1. tar -cvf 解压
2. tar -tvf 压缩列表
3. tar -xvf 解压
