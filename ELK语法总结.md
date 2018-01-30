# ELK
## *Elasticsearch*
## 增删改查
+ 增
1. curl -X PUT 'http://localhost:9200/indexname/_create'
+ 删
1. curl -X DELETE 'http://localhost:9200/indexname'
+ 改
1. curl -X PUT 'http://localhost:9200/indexname/
+ 查
1. curl -X GET 'http://localhost:9200/_search?pretty'

## 增加密码验证
+ 查
1. curl  --user elastic:123456 -XPUT  'http://localhost:9200/_search?pretty'

## *query DSL*
+ match_all
```
 GET _search
{
    "query"
    {
        "match_all":{}
    }
}
```
+ match
```
GET /_search
{
    "query": {
        "match": {
            "instrumentid": 10001100
        }
    }
}
```
+ range
```
GET _search
{
  "query": {
    "range": {
        "instrumentid": {
            "gte":  10001101,
            "lte":   10001104
        }
    }
  }
}
```
    *gt 大于
    gte 大于等于
    lt 小于
    lte 小于等于*


+ term
```
GET _search
{
  "query":{
    "term": { "instrumentid": 10001104}
  }
}
```
+ terms
```
GET _search
{
  "query":{
    "terms": { "instrumentid": [10001104,10001101] }
  }
}
```
+ exists
```

```
+ missing

    *exists 查询和 missing 查询被用于查找那些指定字段中有值 (exists) 或无值 (missing) 的文档。这与SQL中的 IS_NULL (missing) 和 NOT IS_NULL (exists) 在本质上具有共性*
```

```