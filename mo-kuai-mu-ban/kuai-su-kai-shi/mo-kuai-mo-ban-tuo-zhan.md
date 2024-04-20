---
description: >-
  为方便对主题中的重复的部分进行复用（类似于vue等前端框架中的“组件”），运用模块化编程思想，我们可以在sonic本身必要的模板文件之外，定义一些我们自己的模板文件。
---

# 模块模板拓展

模块模板文件只需要在我们的主题目录下即可，但为了方便管理，我们一般将之统一放在一个文件夹中，[sonic默认主题](https://github.com/go-sonic/default-theme-anatole)放在了`module目录`下，开发时可遵循这一规范。

### 定义模块模板

与必要页面的模板文件相同，都需要在html文本外包裹一个模板定义语法

```
{{- define "caicai_anatole/module/sidebar" -}}
...中间的html文本
{{end}}
```

### 调用模块模板

在其他模板文件中使用`template`关键字调用，如sonic默认主题index文件中[调用sider模](https://github.com/go-sonic/default-theme-anatole/blob/master/journals.tmpl#L26)块

```
{{template "caicai_anatole/module/sidebar" .}}
```



