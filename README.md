# mos的官网

[![Netlify Status](https://api.netlify.com/api/v1/badges/7e21993d-e0cb-4030-be1d-b0449ab83e82/deploy-status)](https://app.netlify.com/sites/mos/deploys)

新的官网使用[hexo](https://hexo.io/zh-cn/)搭建，参观地址是[https://mos.dlpu.org/](https://mos.dlpu.org/)。

# 如果你想参与开发或内容贡献 ↓

## 简略方法

前往并fork此[github repo](https://github.com/mos/blog)，修改后提交pull request。或者从master新建分支，修改后提交merge request。

## 安装工具

### 安装nodejs

需要[`nodejs`](http://nodejs.cn/)开发环境，并确保可以流畅使用`npm`（为了确保博客引擎顺利运行，尽量不要使用淘宝提供的`cnpm`）。

### 安装git

需要[`git`](https://git-scm.com/)，并且希望你会用`git add`、`git commit`、`git push`。

### 安装hexo-cli

需要使用`npm`安装`hexo-cli`，在安装了nodejs的终端上使用命令安装：

```shell
npm install -g hexo-cli
```

> 安装`hexo`之后，一切的操作都可以参见[hexo文档](https://hexo.io/zh-cn/docs/)。如果只想提供内容，不需要完全会用hexo，只看这个README即可；否则请阅读hexo文档。

## 提供内容

### 新建文章

在终端使用命令
```shell
hexo new [filename]
```

例如
```shell
hexo new example
```

执行成功后，会自动在`/source/_posts`创建一个`[filename].md`文件和一个`[filename]`文件夹。

md文件是文章内容，文件夹里存放在文章中引用的文件，例如图片。

### 新建页面

文章和页面的区别是，文章会在发布后被收录进`/archive`页面里，但页面不会。

在终端使用命令

```shell
hexo new page [pagename]
```

例如
```shell
hexo new page [example]
```

执行成功后，会在`/source`创建一个`[pagename]`文件夹，`[pagename]/index.md`是页面内容，访问地址是`http://hostname/[pagename]`。

## 生成静态页

生成静态页已经用工具实现，你只需要注重内容本身就可以了。

## 发布

在控制台执行

```shell
git add *
```

将全部修改都添加进暂存区。再执行

```shell
git commit -m 'message'
```

提交当前更改。再执行

```shell
git push
```

将变更推送到github。

接着前往github提交pull request或merge request，合并到原repo的master分支，就可以在[参观地址](https://mos.dlpu.org/)看到了。
