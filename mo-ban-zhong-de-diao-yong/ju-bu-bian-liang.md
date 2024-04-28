# 局部变量

一部分随网页请求而变化的动态数据依靠模板渲染的model来传递，与[全局变量](quan-ju-bian-liang/)类似，只不过仅在对应页面生效

在`github.com/go-sonic/sonic/handler/content/model`目录下的文件中查看——`Render`方法的第二个参数即页面的名称，同函数下的model所拥有的字段即对应页面的可用值

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

在`links`（友情链接）页面中即可使用`{{.is_links}}`来判断是否在`links`页面中（听起来是个很傻的功能，但应该有用吧）

***

sonic共10个[必需页面](../mo-kuai-mu-ban/kuai-su-kai-shi/#bi-xu-ye-mian)10个局部空间

<details>

<summary>index</summary>

is\_index

posts

meta\_keywords

meta\_description

</details>

***

<details>

<summary>archives</summary>

is\_archives

posts

archives

meta\_keywords

meta\_description

</details>

***

<details>

<summary>post</summary>

prePost

nextPost

categories

tags

metas

meta\_description

meta\_keywords

is\_post

target

slug

type

</details>

***

<details>

<summary>post(后台预览)</summary>

post

prevPost

nextPost

categories

tags

metas

meta\_description

meta\_keywords

is\_post

target

type

</details>

***

<details>

<summary>category</summary>

is\_category

slug

type

posts

category

meta\_description

meta\_keywords

</details>

***

<details>

<summary>categories</summary>

is\_categories

meta\_keywords

meta\_description

</details>

***

<details>

<summary>journals</summary>

is\_journals

journals

meta\_keywords

meta\_description

</details>

***

<details>

<summary>links</summary>

is\_links

meta\_keywords

meta\_descriptions

</details>

***

<details>

<summary>photos</summary>

is\_photos

photos

meta\_keywords

meta\_description

</details>

***

<details>

<summary>sheet</summary>

is\_sheet

slug

type

target

post

sheet

tags

metas

meta\_keywords

meta\_description

</details>

***

<details>

<summary>sheet（后台预览）</summary>

target

type

post

sheet

is\_sheet

tags

metas

meta\_keywords

meta\_description

</details>

***

<details>

<summary>tag</summary>

is\_tag

posts

tag

meta\_keywords

meta\_description

</details>

***

<details>

<summary>tags</summary>

is\_tags

meta\_keywords

meta\_description

</details>
