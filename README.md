# gitbook使用说明

## 推送到线上
```python
git add .
git commit -m 'init'
git push -u origin master
git subtree push --prefix=_book origin gh-pages```
*注意过程中需要创建远程连接并输入Github用户名密码*
___
### 本地访问链接
http://localhost:4000

###远程笔记连接
https://FrankHeee.github.io/notes
[远程笔记连接](https://FrankHeee.github.io/notes)
###远程仓库
https://github.com/FrankHeee/notes.git

###启动
`
gitbook serve
`