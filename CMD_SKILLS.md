# Introduction

# 增加系统变量
### 比如今天重新安装了GIT，在CMD命令行中输入 git 回车，反馈说git不是有效的命令云云
### 遂想到系统环境变量问题
### 但是WIN10每次查找并增加系统变量总是很麻烦
### 经查 有如下方法直接在CMD中操作

#查看所有可用的环境变量：
set
#查看某个环境变量
set 变量名
## 如 set path

#修改环境变量 set 变量名=变量内容
## 注意这种方式会直接替换变量，需谨慎操作，尤其是path变量中往往存有大量的环境变量path值，这种方式应使用给变量追加内容的方式

# 给环境变量追加内容：set path=%path%;d\nnnn\dddd\bin
## 如下，给git增加环境变量
set path=%path%;C:\Program Files\Git\bin
# 妈妈再也不用担心我git安装不成功了