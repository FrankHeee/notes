1、云服务器后台运行网站项目
```shell
nohup python manage.py runserver 0.0.0.0:8000 &
```


2、检查服务是否启动list of open files
网站不能访问，需要检查服务器是否在正常运行，通过估计的端口查看进程
```shell
lsof -i:8000
```
# 冒号后面是端口

如端口有多个进程可尝试
```
lsof -i:8000|grep runserver
```
8000是服务启动的端口；runserver是启动该服务时用的命令；管道符“|”的作用是将前一步的数据用后面的字符进行匹配（grep）

3、关于迁移——migrations只针对一个APP进行迁移
```
python manage.py makemigrations --empty 应用名字
```

4、标准HTML模板——来自网友优化
适用PC
```html
<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
    <meta name="renderer" content="webkit" />
    <title>Document</title>
<!--[if lt IE 9]>
    <script src="//cdn.staticfile.org/html5shiv/r29/html5.min.js"></script>
    <script src="//cdn.staticfile.org/respond.js/1.4.2/respond.min.js"></script>
    <script src="//cdn.staticfile.org/es5-shim/4.5.9/es5-shim.min.js"></script>
    <script src="//cdn.staticfile.org/es5-shim/4.5.9/es5-sham.min.js"></script>
<![endif]-->
    <link rel="stylesheet" href="//cdn.staticfile.org/normalize/6.0.0/normalize.min.css">
</head>
<body>
</body>
</html>
```

移动端模板
```html
<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8" />
    <meta name="format-detection" content="telephone=no" />
    <title>Document</title>
    <script>
    (function() {
        var w = 750; // 设计稿尺寸
        document.write('<meta name="viewport" 
						content="width=' + w + ', 
						initial-scale=' + window.screen.width / w + ', 
						user-scalable=0" />');
    })()
    </script>
    <link rel="stylesheet" href="//cdn.staticfile.org/normalize/6.0.0/normalize.min.css">
</head>
<body>
    <script src="//cdn.staticfile.org/fastclick/1.0.6/fastclick.min.js"></script>
    <script>
    document.addEventListener('DOMContentLoaded', function() {
        Origami.fastclick(document.body);
    }, false);
    </script>
</body>
</html>
```
