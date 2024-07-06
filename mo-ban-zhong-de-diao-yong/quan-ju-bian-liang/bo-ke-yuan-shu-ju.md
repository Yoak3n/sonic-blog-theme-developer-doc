# 博客元数据

## **version**

sonic的版本号，默认为`v1.0.0`,定义在 `github.com/go-sonic/sonic/const/const.go`中

## **options**

sonic的系统设置项，定义在`github.com/go-sonic/sonic/model/property`目录下各文件中

```go
var AllProperty = []Property{
	UploadImagePreviewEnable,
	UploadMaxParallelUploads,
	UploadMaxFiles,
	AttachmentType,
	BlogLocale,
	BlogTitle,
	BlogLogo,
	BlogURL,
	BlogFavicon,
	BlogFooterInfo,
	EmailHost,
	EmailProtocol,
	EmailSSLPort,
	EmailUsername,
	EmailPassword,
	EmailFromName,
	EmailIsEnabled,
	EmailStarttls,
	CustomHead,
	CustomContentHead,
	StatisticsCode,
	GlobalAbsolutePathEnabled,
	DefaultEditor,
	PostPermalinkType,
	SheetPermalinkType,
	CategoriesPrefix,
	TagsPrefix,
	ArchivesPrefix,
	SheetPrefix,
	LinksPrefix,
	PhotosPrefix,
	JournalsPrefix,
	PathSuffix,
	IsInstalled,
	Theme,
	BirthDay,
	DefaultMenuTeam,
	SeoKeywords,
	SeoDescription,
	SeoSpiderDisabled,
	SummaryLength,
	RssPageSize,
	RssContentType,
	IndexPageSize,
	ArchivePageSize,
	IndexSort,
	RecycledPostCleaningEnabled,
	RecycledPostRetentionTime,
	RecycledPostRetentionTimeunit,
	APIAccessKey,
	CommentGravatarDefault,
	CommentNewNeedCheck,
	CommentNewNotice,
	CommentReplyNotice,
	CommentAPIEnabled,
	CommentPageSize,
	CommentContentPlaceholder,
	CommentInternalPluginJs,
	CommentGravatarSource,
	CommentBanTime,
	CommentRange,
	MinioEndpoint,
	MinioBucketName,
	MinioAccessKey,
	MinioAccessSecret,
	MinioProtocol,
	MinioSource,
	MinioRegion,
	MinioFrontBase,
	AliOssEndpoint,
	AliOssBucketName,
	AliOssAccessKey,
	AliOssDomain,
	AliOssProtocol,
	AliOssAccessSecret,
	AliOssSource,
	AliOssStyleRule,
	AliOssThumbnailStyleRule,
	HuaweiOssDomain,
	HuaweiOssEndpoint,
	HuaweiOssBucketName,
	HuaweiOssAccessKey,
	HuaweiOssAccessSecret,
	QiniuOssAccessKey,
	QiniuOssAccessSecret,
	QiniuOssDomain,
	QiniuOssBucket,
	QiniuDomainProtocol,
	QiniuOssStyleRule,
	QiniuOssThumbnailStyleRule,
	QiniuOssZone,
	TencentCosDomain,
	TencentCosProtocol,
	TencentCosRegion,
	TencentCosBucketName,
	TencentCosSecretID,
	TencentCosSecretKey,
	TencentCosSource,
	TencentCosStyleRule,
	TencentCosThumbnailStyleRule,
	UpOssSource,
	UpOssPassword,
	UpOssBucket,
	UpOssDomain,
	UpOssProtocol,
	UpOssOperator,
	UpOssStyleRule,
	UpOssThumbnailStyleRule,
	PhotoPageSize,
	JournalPageSize,
	JWTSecret,
}
```

## **context**

博客的基础url地址，用来拼接博客中的网页链接

## **globalAbsolutePathEnabled**

启用全局绝对路径，以保证博客中引用的链接为绝对路径（不确定），默认开启

## **blog\_title**

博客的标题

## **blog\_logo**

博客的图标地址

## **blog\_url**

博客的网站地址

## **seo\_keywords**

为搜索引擎优化提供的关键词

## **seo\_description**

为搜索引擎优化提供的描述

## **rss\_url**

博客rss订阅的网页链接

## **atom\_url**

博客atom订阅的网页链接

## **sitemap\_xml\_url**

博客网站地图的XML链接

## **sitemap\_html\_url**

博客网站地图的HTML链接

## **links\_url**

博客友情链接的网页链接

## **photos\_url**

博客照片墙的网页链接

## **journals\_url**

博客日志的网页链接

## **archives\_url**

博客文章归档的网页链接

## **categories\_url**

博客分类目录的网页链接

## **tags\_url**

博客标签列表的网页链接
