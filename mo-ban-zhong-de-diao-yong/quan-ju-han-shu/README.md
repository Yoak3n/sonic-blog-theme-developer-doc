# 全局函数

定义在`github.com/go-sonic/sonic/template`目录下各文件中的全局函数，供模板渲染调用 大致分为博客工具函数和模块数据函数

在模板中调用函数的格式：

```
{{函数名 第1个参数 第2个参数 ...}}
```

**如：**

```
{{unix_milli_time_format "2006-01-02 15:04:05" .post.UpdateTime}}
```

