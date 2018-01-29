## ELK
### Elasticsearch
#### 增删改查
+ 增
1. curl -X PUT 'http://localhost:9200/indexname/_create'
+ 删
1. curl -X DELETE 'http://localhost:9200/indexname'
+ 改
1. curl -X PUT 'http://localhost:9200/indexname/
+ 查
1. curl -X GET 'http://localhost:9200/_search?pretty'
