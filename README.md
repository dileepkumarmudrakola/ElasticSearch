# ElasticSearch

 curl -H "Content-Type: application/json" -XGET "10.0.100.237:9200/filebeat-7.15.2-2021.12.09-000004/_search?size=0&pretty" -d '
 {
     "aggs" : {
        "min_date": {"min": {"field": "@timestamp", "format": "yyyy-MM-dd"}},
        "max_date": {"max": {"field": "@timestamp", "format": "yyyy-MM-dd"}}
     }
}
'
