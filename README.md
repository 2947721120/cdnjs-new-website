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
