---
description: 用于各个页面所需的获取后台数据的函数
---

# 数据函数

示例（获取分类列表并赋给变量`$list`以在该模板中方便地调用）：

```
{{ $list := listCategory }} 
```

> ## **分类**

<details>

<summary>category.go</summary>

## 1.listCategory

返回一个带有各分类所含文章数目的分类列表

## **2.listCategoryAsTree**

返回一个树状的分类目录列表

## **3.listCategoryByPostID**

根据文章的id返回一个该文章所属的分类列表

## **4.getCategoryCount**

获取所有分类的数目

</details>

***

> ## **评论数据**

<details>

<summary>comment.go</summary>

## **1.getLatestComment**

获取各文章最新的评论，返回一个以**评论列表**及其**所属文章**为单位的列表

## **2.getCommentCount**

获取总公开评论数

</details>

***

> ## 友情链接

<details>

<summary>link.go</summary>

## **1.listLinks**

返回一个普通的友情链接列表

## **2.listLinksRandom**

返回一个被刻意打乱顺序的友情链接列表

## **3.listLinksGroupByTeam**

返回一个标签分组的map，key为组别，value为标签链接列表

## **4.getLinksCount**

返回友情链接的数目

</details>

***

> ## **菜单**

<details>

<summary><strong>menu.go</strong></summary>

## **1.listMenu**

返回一个菜单设置的列表

## **2.listMenuAsTree**

返回一个菜单设置的树状列表

## **3.listMenuTeams**

返回一个菜单组别的列表

## **4.listMenuByTeam**

根据分组名返回对应的菜单设置列表

## **5.listMenuAsTreeByTeam**

根据分组名返回对应的树状菜单设置列表（？）

## **6.getMenuCount**

返回菜单设置数目

</details>

***

> ## 分页

<details>

<summary><strong>pagination.go</strong></summary>

示例函数：

```go
func indexPagination(page, total, display int) (*vo.Pagination, error) 
```

**分页数据**`Pagination`结构体包含了`RainbowPages`彩虹分页列表，`PrevPageFullPath`上一页绝对路径，`NextPageFullPath`下一页绝对路径以及是存在上下页的HasPrev、HasNext

## **1.indexPagination**

根据当前页数`page`，所有文章数`total`与每一页文章数`display`计算出index博客入口页面的**分页数据**

## **2.archivesPagination**

根据当前页数`page`，所有文章数`total`与每一页文章数`display`计算出当前archives文章归档页面的**分页数据**

## **3.searchPagination**

根据当前页数`page`，所有文章数`total`与每一页文章数`display`计算出当前search搜索页面的**分页数据**

## **4.tagPostsPagination**

根据当前页数`page`，所有文章数`total`与每一页文章数`display`计算出当前tag标签页面的**分页数据**

## **5.categoryPostsPagination**

根据当前页数`page`，所有文章数`total`与每一页文章数`display`计算出当前category文章分类页面的**分页数据**

## **6.photosPagination**

根据当前页数`page`，所有文章数`total`与每一页文章数`display`计算出当前photos相册页面的**分页数据**

## **7.journalsPagination**

根据当前页数`page`，所有文章数`total`与每一页文章数`display`计算出当前journals日志页面的**分页数据**

</details>

***

> ## 相册

<details>

<summary><strong>photo.go</strong></summary>

## **1.listPhotos**

返回一个相册列表

## **2.listTeamPhotos**

返回一个以分组为key，以照片列表为value的map

## **3.listPhotoByTeam**

根据分组名返回对应照片列表

## **4.getPhotoCount**

返回所照片的数目

</details>

***

> ## 文章

<details>

<summary><strong>post.go</strong></summary>

## **1.listLatestPost**

返回一个根据发布时间排序的最新文章列表，需填入这个列表的限制长度

## **2.listMostPopularPost**

返回一个根据访问数排序的最热文章列表，需填入这个列表的限制长度

## **3.getPostCount**

返回所有文章的数目

## **4.listYearArchives**

返回一个以**文章列表**及其**所属年份**为单位的列表

## **5.listMonthArchives**

返回一个以**文章列表**及其**所属月份**为单位的列表

## **6.listPostByCategoryID**

根据**分类id**返回一个对应的文章列表

## **7.listPostByCategorySlug**

根据**分类别名**返回一个对应的文章列表

## **8.listPostByTagID**

根据**标签id**返回一个对应的文章列表

## **9.listPostByTagSlug**

根据**标签别名**返回一个对应的文章列表

</details>

***

> ## 标签

<details>

<summary><strong>tag.go</strong></summary>

## **1.getAllTag**

返回一个包含所有标签（带所属文章数目）的列表

## **2.getTagByPostID**

根据文章id，返回对应的标签列表

## **3.getTagCount**

返回所有标签的数目

</details>

***

> ## 全局静态数据

<details>

<summary><strong>static.go</strong></summary>

## **getStatisticsData**

返回一个名为`Statistic`的结构体

```go
type Statistic struct {
    PostCount     int64 `json:"postCount"`
    CommentCount  int64 `json:"commentCount"`
    CategoryCount int64 `json:"categoryCount"`
    TagCount      int64 `json:"tagCount"`
    JournalCount  int64 `json:"journalCount"`
    Birthday      int64 `json:"birthday"`
    EstablishDays int64 `json:"establishDays"`
    LinkCount     int64 `json:"linkCount"`
    VisitCount    int64 `json:"visitCount"`
    LikeCount     int64 `json:"likeCount"`
}
```

PostCount：博客文章数

CommentCount：博客评论数

CategoryCount：博客分类数

TagCount：博客标签数

JonrnalCount：博客日志数

Birthday：博客开始时间（时间戳）

EstablishDays：博客存在时间（时间间隔）

LinkCount：博客友情链接数

VisitCount：博客访问数

LikeCount：博客点赞数

</details>
