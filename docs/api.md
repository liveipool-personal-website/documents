# Liveipool-Personal-Website API

<!-- MarkdownTOC -->

- [返回状态说明](#返回状态说明)
    - [状态码](#状态码)
- [主页](#主页)
    - [获取主页大背景图](#获取主页大背景图)
    - [获取主页小背景图](#获取主页小背景图)
    - [获取主页提示语](#获取主页提示语)

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

