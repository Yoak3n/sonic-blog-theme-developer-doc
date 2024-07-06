# 主题配置

在主题根目录的`settings.yaml`或`settings.yml`中定义主题的设置项

参考[sonic默认主题的settings.yaml](https://github.com/go-sonic/default-theme-anatole/blob/master/settings.yaml)展示于`主题设置>关于`之后的标签页

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

```
style:
  label: 样式设置
  items:
    sidebar_width:
      name: sidebar_width
      label: 侧边栏宽度
      type: select
      data-type: string
      default: '40%'
      options:
        - value: '20%'
          label: '20%'
        - value: '30%'
          label: '30%'
        - value: '40%'
          label: '40%'
        - value: '50%'
          label: '50%'
```

***

## 配置字段

**使用yaml语法进行定义**

### 标签页

一级字段（如上面的`style`，可自定义字段名)标识一个设置的标签页

二级字段（`label`，固定字段名）表示该标签页展示出来的标签名

二级字段（`items`，固定字段名）表示该标签页所包含的设置项

### 设置项

items的子项(如上面的`sidebar_width`，是可自定义字段)，标识一个**设置项**

设置项应包含如下子项：

* name
* label
* type

#### name

该设置项的名称

#### label

该设置项展示出来的标签名

#### type

设置项的类型，可选值有：text、textarea、radio、select和attachment等

{% hint style="info" %}
以下为可选的字段
{% endhint %}

#### placeholder

当设置项的类型为text或textarea时，设置文本输入框的占位文字

#### options

当设置项的类型为select或radio时，为该设置项提供选项，options的子项为yaml格式的数组，数组元素有`value`和`label`属性

```yaml
options:
  - value: true
    label: 开启
  - value: false
    label: 关闭
```

#### default

该设置项的默认值

#### data-type

指定设置项返回的值类型，可选值有：string、int64、bool等

#### description

该设置项的描述内容

***

<details>

<summary>如何使用主题设置中的值？</summary>

查看模板调用全局变量[主题设置](../mo-ban-zhong-de-diao-yong/quan-ju-bian-liang/zhu-ti-shu-xing.md#settings)的部分

</details>
