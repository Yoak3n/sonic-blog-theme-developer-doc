# sonic主题开发者文档

## 前言

[sonic](https://github.com/go-sonic/sonic)主题开发主要使用golang的模板渲染引擎，因此需要具有对golang模板解析[基本语法](https://pkg.go.dev/html/template)的了解，以及必备的一定前端基础后，再开始我们的主题开发。

## 目录结构

主题所需文件的目录结构大致如下：

<pre><code>|--archives.tmpl --> 所有文章归档页面
<strong>|--categories.tmpl --> 文章分类目录页面
</strong>|--category.tmpl --> 单个文章分类页面
|--index.tmpl --> 博客入口页面
|--journals.tmpl --> 博客日志页面
<strong>|--inks.tmpl --> 博客友情链接页面
</strong>|--post.tmpl --> 单个文章页面
|--search.tmpl --> 博客搜索结果页面
|--sheet.tmpl --> 博客关于页面
<strong>|--tags.tmpl --> 文章标签目录页面
</strong>|--tag.tmpl --> 单个文章标签页面
(以上tmpl模板文件为博客主题必要的文件,对应sonic默认存在的页面)
|--screenshot.png --> 主题预览图  
|--README.md --> 主题的说明文档  
|--settings.yaml --> 主题的设置项目(必要)  
|--theme.yaml --> 主题的基本信息(必要)
(以下为拓展部分，可按照自身开发习惯自行设计）
|--assets --> 一般是存放主题的静态资源，如图片、字体、CSS、JavaScript等  
|--module --> 存放主题的模块文件，如header.tmpl、footer.tmpl等，方便模块的复用  
      |--footer.tmpl --> 页脚模块模板  
      |--header.tmpl --> 页眉模块模板  
      |--style.tmpl --> 样式模块模板  
      |--...  
</code></pre>
