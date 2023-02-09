---
title: KinhRelay v1.0.0
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - ruby: Ruby
  - python: Python
  - php: PHP
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
code_clipboard: true
highlight_theme: darkula
headingLevel: 2
generator: "@tarslib/widdershins v4.0.17"

---

# KinhRelay

> v1.0.0

Base URLs:

# Default

## PUT 插入队列

PUT /Relay.php

> Body 请求参数

```json
{
  "Listen_Address": "127.0.0.1",
  "Listen_Port": 9800,
  "Remote_Address": "127.0.0.1",
  "Remote_Port": 9808,
  "MaxSpeed": 0,
  "MaxConnect": 0,
  "ShieldAgreement": {
    "Socks5": false,
    "TLS": {
      "But": false,
      "Not": false
    }
  },
  "IPWhiteList": [
    "127.0.0.1"
  ]
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|object| 否 ||none|
|» Listen_Address|body|string| 是 | 监听地址|监听地址|
|» Listen_Port|body|integer| 是 | 监听端口|监听端口|
|» Remote_Address|body|string| 是 | 远程地址|远程地址|
|» Remote_Port|body|integer| 是 | 远程端口|远程端口|
|» MaxSpeed|body|integer| 是 | 最大速率|最大速率|
|» MaxConnect|body|integer| 是 | 最大连接数|最大连接数|
|» ShieldAgreement|body|object| 是 | 屏蔽协议|屏蔽协议|
|»» Socks5|body|boolean| 是 | 是否屏蔽Socks5协议|是否屏蔽Socks5协议|
|»» TLS|body|object| 是 | 屏蔽TLS协议|屏蔽TLS协议|
|»»» But|body|boolean| 是 | 是否屏蔽TLS协议|是否屏蔽TLS协议|
|»»» Not|body|boolean| 是 | 是否屏蔽非TLS协议|是否屏蔽非TLS协议|
|» IPWhiteList|body|[string]| 是 | IP白名单|IP白名单|

> 返回示例

> 成功

```json
{
  "Message": "成功",
  "Status": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» Message|string|true|none|信息|信息|
|» Status|integer|true|none|状态|状态|

## GET 获取队列

GET /Relay.php

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|ResetFlow|query|string| 是 ||重置流量|

> 返回示例

> 成功

```json
{
  "9800": {
    "Listen_Address": "127.0.0.1",
    "Listen_Port": 9800,
    "Remote_Address": "127.0.0.1",
    "Remote_Port": 9808,
    "MaxSpeed": 0,
    "MaxConnect": 0,
    "ShieldAgreement": {
      "NonTLS": false,
      "Socks5": false
    },
    "IPWhiteList": [
      "127.0.0.1"
    ],
    "Delay": {
      "StartTime": 0,
      "EndTime": 0,
      "MicroSeconds": 0
    },
    "Flow": 0,
    "Error": "正常"
  },
  "Message": "成功",
  "Status": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» 9800|object|true|none|端口|端口|
|»» Listen_Address|string|true|none|监听地址|监听地址|
|»» Listen_Port|integer|true|none|监听端口|监听端口|
|»» Remote_Address|string|true|none|远程地址|远程地址|
|»» Remote_Port|integer|true|none|远程端口|远程端口|
|»» MaxSpeed|integer|true|none|最大速率|最大速率|
|»» MaxConnect|integer|true|none|最大连接数|最大连接数|
|»» ShieldAgreement|object|true|none|屏蔽协议|屏蔽协议|
|»»» Socks5|boolean|true|none|是否屏蔽Socks5协议|是否屏蔽Socks5协议|
|»»» TLS|object|true|none|屏蔽TLS协议|屏蔽TLS协议|
|»»»» But|boolean|true|none|是否屏蔽TLS协议|是否屏蔽TLS协议|
|»»»» Not|boolean|true|none|是否屏蔽非TLS协议|是否屏蔽非TLS协议|
|»» IPWhiteList|[string]|true|none|IP白名单|IP白名单|
|»» Delay|object|true|none|延迟|延迟|
|»»» StartTime|integer|true|none|连接开始时间|连接开始时间|
|»»» EndTime|integer|true|none|连接完成时间|连接完成时间|
|»»» MicroSeconds|integer|true|none|毫秒|毫秒|
|»» Flow|integer|true|none|流量|流量|
|»» Error|string|true|none|错误|错误|
|» Message|string|true|none|信息|信息|
|» Status|integer|true|none|状态|状态|

## DELETE 移除队列

DELETE /Relay.php

> Body 请求参数

```json
{
  "Listen_Port": 9800
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|object| 否 ||none|
|» Listen_Port|body|integer| 是 | 监听端口|监听端口|

> 返回示例

> 成功

```json
{
  "Message": "成功",
  "Status": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» Message|string|true|none|信息|信息|
|» Status|integer|true|none|状态|状态|

## PATCH 更改队列数据

PATCH /Relay.php

> Body 请求参数

```json
{
  "Listen_Port": 9800,
  "Remote_Address": "127.0.0.1",
  "Remote_Port": 9808,
  "MaxSpeed": 0,
  "MaxConnect": 0,
  "ShieldAgreement": {
    "Socks5": false,
    "TLS": {
      "But": false,
      "Not": false
    }
  },
  "IPWhiteList": [
    "127.0.0.1"
  ]
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|object| 否 ||none|
|» Listen_Port|body|integer| 是 | 监听端口|监听端口|
|» Remote_Address|body|string| 是 | 远程地址|远程地址|
|» Remote_Port|body|integer| 是 | 远程端口|远程端口|
|» MaxSpeed|body|integer| 是 | 最大速率|最大速率|
|» MaxConnect|body|integer| 是 | 最大连接数|最大连接数|
|» ShieldAgreement|body|object| 是 | 屏蔽协议|屏蔽协议|
|»» Socks5|body|boolean| 是 | 是否屏蔽Socks5协议|是否屏蔽Socks5协议|
|»» TLS|body|object| 是 | 屏蔽TLS协议|屏蔽TLS协议|
|»»» But|body|boolean| 是 | 是否屏蔽TLS协议|是否屏蔽TLS协议|
|»»» Not|body|boolean| 是 | 是否屏蔽非TLS协议|是否屏蔽非TLS协议|
|» IPWhiteList|body|[string]| 是 | IP白名单|IP白名单|

> 返回示例

> 成功

```json
{
  "Message": "成功",
  "Status": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» Message|string|true|none|信息|信息|
|» Status|integer|true|none|状态|状态|

# 数据模型

