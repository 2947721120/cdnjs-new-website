new-website
===========

前端网站(不含公共库)https://cdnjs.com，为CDN内容，请参阅[cdnjs/cdnjs](https://github.com/cdnjs/cdnjs) 回购

[![Dependency Status](https://david-dm.org/cdnjs/new-website.svg?theme=shields.io)](https://david-dm.org/cdnjs/new-website) [![Issue Stats](http://www.issuestats.com/github/cdnjs/new-website/badge/pr?style=flat)](http://www.issuestats.com/github/cdnjs/new-website) [![Issue Stats](http://www.issuestats.com/github/cdnjs/new-website/badge/issue?style=flat)](http://www.issuestats.com/github/cdnjs/new-website)

## 依赖

* [Node](https://nodejs.org)
* [MongoDB](https://mongodb.org)

## 建立

```sh
cd path/to/repo
npm install
```

## 运行

```sh
MONGOHQ_URL=<mongodb url>
APP=[mainSite|api]
./runServer.sh
```

**Note**:

 * 确保 `mongod`的是，如果您使用的是本地数据库上运行。
 * 的工件/元数据是关于所述 [meta](https://github.com/cdnjs/new-website/tree/meta) 分支

**Heads up**: `runServer.sh` 脚本只适用于本地运行。如果你使用的是其他shell中运行节点[web服务器| API服务器]  `node [webServer|apiServer].js` 文件来代替。

##API查询
您可以通过的API搜索
```
https://api.cdnjs.com/libraries
```
没有任何查询参数将返回的名称和每一个图书馆的主要文件的URL在CDNJS。搜索，使用：

```
https://api.cdnjs.com/libraries?search=jquery
```

API将收益缩小结果的默认情况下，如果你想拥有一个人类可读的结果，尝试 `output=human` 像这样：

```
https://api.cdnjs.com/libraries?output=human
https://api.cdnjs.com/libraries?search=jquery&output=human
```

如果您想了解更多的资料，请使用fields参数这需要逗号分隔值：

```
https://api.cdnjs.com/libraries?search=jquery&fields=version,description
```

要获得该库的所有文件的列表，使用该文件字段：

```
https://api.cdnjs.com/libraries?search=jquery&fields=assets
```

其他领域可用：

```
version//版本
description//描述
homepage//首页
keywords//关键词
maintainers//维护
assets//文件
```

API服务超过一六小时届满请求CloudFlare


