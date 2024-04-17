# 主题设置

在主题根目录的`setting.yaml`或`setting.yml`中定义主题的设置项

参考[sonic默认主题的setting.yaml](https://github.com/go-sonic/default-theme-anatole/blob/master/settings.yaml)展示于`主题设置>关于`之后的标签页

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

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

使用yaml语法进行定义

### 标签页

一级字段（如上面的`style`，可自定义)标识一个设置的标签页

二级字段（`label`，不可更名）表示该标签页展示出来的名称

二级字段（`items`，不可更名）表示该标签页所包含的设置项

### 设置项

items的子项(如上面的`sidebar_width`)，标识一个**设置项**

设置项包含如下子项：

* name
* label
* type
* data-type
* default

