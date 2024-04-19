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

获取各文章最新的评论，返回一个以评论及其所属文章为单位的列表

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

返回一个树状菜单设置的列表

## **3.listMenuTeams**

返回菜单分组的列表

## **4.listMenuByTeam**

返回

## **5.listMenuAsTreeByTeam**

返回一个树状菜单

## **6.getMenuCount**

返回

</details>

***

> ## 分页

<details>

<summary><strong>pagination.go</strong></summary>

## **1.indexPagination**

## **2.archivesPagination**

## **3.searchPagination**

## **4.tagPostsPagination**

## **5.categoryPostsPagination**

## **6.photosPagination**

## **7.journalsPagination**

</details>

***

> ## 相册

<details>

<summary><strong>photo.go</strong></summary>

## **1.listPhotos**

## **2.listTeamPhotos**

## **3.listPhotoByTeam**

## **4.getPhotoCount**

</details>

***

> ## 文章

<details>

<summary><strong>post.go</strong></summary>

**1.listLatestPost**

**2.listMostPopularPost**

**3.getPostCount**

**4.listYearArchives**

**5.listMonthArchives**

**6.listPostByCategoryID**

**7.listPostByCategorySlug**

**8.listPostByTagID**

**9.listPostByTagSlug**

</details>

***

> ## 标签

<details>

<summary><strong>tag.go</strong></summary>

## **1.getAllTag**

## **2.getTagByPostID**

## **3.getTagCount**

</details>

***

> ## 全局静态数据

<details>

<summary><strong>static.go</strong></summary>

## **getStatisticsData**

</details>
