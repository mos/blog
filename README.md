# mos的官网

新的官网使用[hexo](https://hexo.io/zh-cn/)搭建，参观地址是[https://mos.github.io/](https://mos.github.io/)。

# 如果你想参与开发或内容贡献 ↓

## 简略方法

前往并fork此[github repo](https://github.com/mos/mos.github.io)，修改后提交pr。

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

全部关于`hexo`的操作都在`/hexo_source`下进行。

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

> 如果你的系统环境是`linux`或`macOS`，可以在`hexo_source`目录下直接执行`./build.sh`，即可一次完成下边描述的全部生成操作。这是为你准备的一键生成脚本。

在完成每一次的修改后，需要在`/hexo_source`目录下执行

```shell
hexo clean && hexo g
cp -rf public/* ../
```

来生成静态页，并复制静态页到根目录。

生成静态页后，需要上传到github来使改动对外可见。

## 发布

> 如果你的系统环境是`linux`或`macOS`，可以在`/`下或`/hexo_source`下执行`./git_publish.sh 'message'`，即可一次完成下边描述的全部上传操作。这是为你准备的一键git push脚本。

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

接着前往github提交pull request，合并到原repo的master分支，就可以在[参观地址](https://mos.github.io/)看到了。

> 由于hexo的问题，同步项目的时候不要将任何文件和文件夹添加到`.gitignore`，特别是`node_modules`，需要全部上传到git中，并同步给每一个参与者。hexo项目虽然由npm创建，但是缺少组件的时候无法使用`npm install`安装，并且会导致`hexo g`失败。