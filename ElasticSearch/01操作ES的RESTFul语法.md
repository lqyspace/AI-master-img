[TOC]

# 操作ES的RESTFul语法

> GET请求：
>
> ​	http://ip:port/index  查询索引信息
>
> ​	http://ip:port/index/type/doc_id   查询指定的文档信息
>
> POST请求：
>
> ​	http://ip:port/index/type/_search：查询文档，可以在请求体中添加json字符串来代表查询条件
>
> ​	http://ip:port/index/type/doc_id/_update：修改文档，在请求体中指定json字符串代表修改的具体信息
>
> PUT请求：
>
> ​	http://ip:port/index  创建一个索引，需要在请求体中指定索引的信息，类型，结构
>
> ​	http://ip:port/index/type/_mappings  代表创建索引时，指定索引文档存储的属性的信息
>
> DELETE请求：
>
> ​	http://ip:port/index   删库
>
> ​	http://ip:port/index/type/doc_id  删除指定的文档



## 创建索引

```js
# 创建一个索引
PUT /person
{
  "settings": {
    "number_of_shards": 5,
    "number_of_replicas": 1
  }
}
```

## 查看索引信息

```js
# 查看索引信息
GET /person
```

![image-20240822163415968](https://fastly.jsdelivr.net/gh/lqyspace/AI-master-img@master/img/202408221634014.png)

## 删除索引

```js
# 删除索引
DELETE /person
```

