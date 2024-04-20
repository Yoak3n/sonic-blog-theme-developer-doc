# 局部变量

一部分随网页请求而变化的动态数据依靠模板渲染的model来传递，与[数据函数](../quan-ju-han-shu/shu-ju-han-shu.md)类似，只不过仅在对应页面生效

在`github.com/go-sonic/sonic/model`目录下的文件中查看——`ThemeService.Render`的第二个参数即页面的名称，同函数下的model所拥有的字段即对应页面的可用值

如：

```go
func (l *LinkModel) Links(ctx context.Context, model template.Model) (string, error) {
    model["is_links"] = true
    model["meta_keywords"] = l.OptionService.GetOrByDefault(ctx, property.SeoKeywords)
    model["meta_description"] = l.OptionService.GetOrByDefault(ctx, property.SeoDescription)
    return l.ThemeService.Render(ctx, "links")
}
```

表示`links`（友情链接）页面中有`is_links,meta_keywords`和`meta_description`三个字段的值

