# 主题属性

## **theme\_base**

当前博客主题的文件所在的目录

## **theme**

当前博客主题的基本信息，如id，name和author等，大部分在`theme.yaml`中进行[配置](../../zhu-ti-xin-xi/ji-ben-xin-xi.md)

如：

```
{{.theme.author}}
```

## **settings**

当前博客主题的设置信息，在`settings.yaml`中进行[配置](../../zhu-ti-xin-xi/zhu-ti-pei-zhi.md)

`settings.yaml`中的[设置项](../../zhu-ti-xin-xi/zhu-ti-pei-zhi.md#she-zhi-xiang)就是settings的属性，如获取[默认主题配置](https://github.com/go-sonic/default-theme-anatole/blob/master/settings.yaml)中侧边栏宽度：

```
{{.settings.sidebar_width}}
```
