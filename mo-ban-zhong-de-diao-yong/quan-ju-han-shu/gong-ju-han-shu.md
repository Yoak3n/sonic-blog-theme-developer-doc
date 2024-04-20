# 工具函数

## **unix\_milli\_time\_format**

```go
func unix_milli_time_format(format string, t int64) string
```

时间格式化工具函数，第1个参数为golang特殊的时间格式化字符串模板，第2个参数是一个int64类型的时间戳

## **noescape**

```go
func noescape(str string) htmlTemplate.HTML
```

插入html文本的工具函数，参数为一个类型为字符串的html文本

## **rainbowPage**

```go
func rainbowPage(page, total, display int) []int
```

彩虹分页算法。

接受三个参数：`page`（当前页码），`total`（总数据条数），`display`（每页显示的数据条数）。函数会根据参数计算出页码对应的数字列表，返回这个列表。假设我们有一个包含10个数据的大组，每页显示3个数据，当前请求的页码为2。那么函数会返回一个包含数字`{1, 2, 3}`的切片。——来自Codegeex

## **random**

```go
func random(min, max int) int
```

随机数生成，返回一个范围是\[min,max)的随机数

## [**sprig**](https://github.com/Masterminds/sprig)

第三方库提供的可在模板中使用的函数，可参阅其[function documentation](http://masterminds.github.io/sprig/)
