# Liveipool-Personal-Website API

<!-- MarkdownTOC -->

- [返回状态说明](#返回状态说明)
    - [状态码](#状态码)
- [主页](#主页)
    - [获取主页大背景图](#获取主页大背景图)
    - [获取主页小背景图](#获取主页小背景图)
    - [获取主页提示语](#获取主页提示语)
- [博客页面](#博客页面)
    - [获取文章类别列表](#获取文章类别列表)
    - [获取文章信息列表](#获取文章信息列表)
    - [获取文章内容](#获取文章内容)
- [关于作者页面](#关于作者页面)
    - [获取作者个人信息](#获取作者个人信息)

<!-- /MarkdownTOC -->

<a name="返回状态说明"></a>
## 返回状态说明

一个请求是否成功是由 HTTP 状态码标明的。不同的状态码对应了不同的请求状态，具体各状态码及信息待完善。

<a name="状态码"></a>
### 状态码
待完善

| Code | HTTP Status | Description |
|:----:|:-----------:|-------------|
|0|200|请求成功。
|1|404|资源未找到。

<a name="主页"></a>
## 主页

<a name="获取主页大背景图"></a>
### 获取主页大背景图

Request URI:

```
GET /home/bigBackPic
```

Response Properties:

| Property | Description | Type |
|----------|-------------|------|
|url|大背景图的url|string|

Response Example:

```json
{
    "url": "http://123.123.123.123/big.png"
}
```

<a name="获取主页小背景图"></a>
### 获取主页小背景图

Request URI:

```
GET /home/smallBackPic
```

Response Properties:

| Property | Description | Type |
|----------|-------------|------|
|url|小背景图的url|string|

Response Example:

```json
{
    "url": "http://123.123.123.123/small.png"
}
```

<a name="获取主页提示语"></a>
### 获取主页提示语

Request URI:

```
GET /home/slogan
```

Response Properties:

| Property | Description | Type |
|----------|-------------|------|
|slogan|主页提示语|string|

Response Example:

```json
{
    "slogan": "李为的个人网站"
}
```

<a name="博客页面"></a>
## 博客页面

<a name="获取文章类别列表"></a>
### 获取文章类别列表

Request URI:

```
GET /blog/categorys
```

Response Properties:

| Property | Description | Type |
|----------|-------------|------|
|categorys|文章类别列表|string array|

Response Example:

```json
{
    "categorys": ["前端", "后端", "英语", "数学"]
}
```

<a name="获取文章信息列表"></a>
### 获取文章信息列表

Request URI:

```
GET /blog/blogInfos/:start/:count
```

Request Properties:

| Property | Description | Type |
|----------|-------------|------|
|start|从第几篇对应类别的文章开始|number|
|count|一共要请求多少篇文章的信息|number|

Response Properties:

| Property | Description | Type |
|----------|-------------|------|
|blogInfos|文章信息列表|object array|
|blogInfos.blogId|文章的id|number|
|blogInfos.title|文章的标题|string|
|blogInfos.uploadDate|文章的上传日期|string|
|blogInfos.category|文章的类别|string|

Response Example:

```json
{
    "blogInfos": [
        {
            "blogId": 0,
            "title": "如何评价中山大学",
            "uploadDate": "2018-03-12",
            "category": "前端",
        },
        {
            "blogId": 1,
            "title": "星巴克焦糖咖啡星冰乐",
            "uploadDate": "2018-02-14",
            "category": "后端"
        }
    ]
}
```

<a name="获取文章内容"></a>
### 获取文章内容

Request URI:

```
GET /blog/:blogId
```

Request Properties:

| Property | Description | Type |
|----------|-------------|------|
|blogId|文章的id|number|

Response Properties:

| Property | Description | Type |
|----------|-------------|------|
|blog|文章内容|object|
|blog.blogId|文章的id|number|
|blog.title|文章的标题|string|
|blog.uploadDate|文章的上传日期|string|
|blog.content|文章的内容|string|

Response Example:

```json
{
    "blog": {
        "blogId": 0,
        "title": "如何评价中山大学",
        "uploadDate": "2018-03-12",
        "content": "..."
    }
}
```

<a name="关于作者页面"></a>
## 关于作者页面

<a name="获取文章类别列表"></a>
### 获取文章类别列表

Request URI:

```
GET /about/personalInfo
```

Response Properties:

| Property | Description | Type |
|----------|-------------|------|
|personalInfo|个人信息|object|
|personalInfo.wechat|微信号|string|
|personalInfo.email|邮箱|string|
|personalInfo.github|github地址|string|

Response Example:

```json
{
    "personalInfo": {
        "wechat": "liveipool",
        "email": "123456789@qq.com",
        "github": "https://github.com/Liveipool"
    }
}
```