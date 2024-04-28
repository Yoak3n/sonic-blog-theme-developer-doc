# 快速开始

在开篇的[目录结构](../../#mu-lu-jie-gou)中简单地了解了一个sonic主题中包含的文件，那么我们就已经可以编写出一个看起来像是来自洪荒时代的sonic主题模板（只保证基本运行的毛坯房）

### 必需页面

1. index.tmpl
2. archives.tmpl
3. category.tmpl
4. journals.tmpl
5. links.tmpl
6. post.tmpl
7. search.tmpl
8. sheet.tmpl&#x20;
9. tags.tmpl&#x20;
10. tag.tmpl

`theme.yaml`是必须文件，否则无法在主题页面切换该主题，如一个最简单的例子：

```yaml
id: sonic_theme_base
name: base
```

只需要编辑一些主题的信息，即可在sonic的后台管理与页面中**看到**我们的毛坯主题：

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

`settings.yaml`是可选文件，但缺失则无法进行主题设置

同理，如果上面的[必需页面](./#bi-xu-ye-mian)中缺失了其中一个，对应的页面也就无法显示

基础主题的文件数目过多，放在文档中太臃肿，这里就算了

{% content-ref url="mo-ban-ji-ben-ge-shi.md" %}
[mo-ban-ji-ben-ge-shi.md](mo-ban-ji-ben-ge-shi.md)
{% endcontent-ref %}

{% content-ref url="mo-kuai-mo-ban-tuo-zhan.md" %}
[mo-kuai-mo-ban-tuo-zhan.md](mo-kuai-mo-ban-tuo-zhan.md)
{% endcontent-ref %}
