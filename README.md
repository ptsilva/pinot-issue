# pinot-issue
Repo for reproduce a possible issue in apache pinot

Steps to reproduce

```shell
docker run -v $(pwd):/data winedepot/pinot:kafka2 CreateSegment \
-dataDir /data/invalid \
-format CSV \
-outDir /data/out \
-tableName table_a \
-segmentName table_name \
-overwrite \
-schemaFile \
/data/schema.json \
-readerConfigFile \
/data/record-reader.json
```

