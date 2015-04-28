---
layout: simple
title: About
---

### 了解：

* markdown: [http://www.appinn.com/markdown/](http://www.appinn.com/markdown/)
* jekyll: [http://jekyll.bootcss.com/docs/frontmatter/](http://jekyll.bootcss.com/docs/frontmatter/)
* sass: [http://www.ruanyifeng.com/blog/2012/06/sass.html](http://www.ruanyifeng.com/blog/2012/06/sass.html), [http://www.w3cplus.com/sassguide/](http://www.w3cplus.com/sassguide/)
* git 的使用，SourceTree 即可。


### 准备工作：

nswbmw 将 gary, malu, lingdang 添加为该库的 Collaborators。

设计师需要安装：

    node.js  ->  https://nodejs.org/download/
    gem install jekyll
    gem install rouge
    gem install sass
    npm install -g grunt-cli

### 第 1 步：

    git clone https://github.com/zhaokun/primer.git

### 第 2 步：

到 primer 目录下运行：

    jekyll serve

启动 jekyll 服务，浏览器打开 `http://127.0.0.1:4000/primer/` 用于本地调试。

sass 文件在 scss 目录下，以后修改样式就是修改这个目录下的样式文件。style guide 文档在 docs 目录下，修改完样式修改对应的 markdown 文件然后重新运行 `jekyll serve`，刷新页面即可看到效果。

**Tips:** `_include` 目录存放了左侧的列表，新建 scss 文件后需要在 docs/docs.scss 文件内引入。

### 第 3 步

每次修改后，首先用 SourceTree 提交修改到 master 分支，然后运行：

    grunt publish

会自动将 master 的修改推送到 GitHub 库的 gh-pages 分支，浏览器打开 `http://zhaokun.github.io/primer/`，可能会过几分钟才生效。
