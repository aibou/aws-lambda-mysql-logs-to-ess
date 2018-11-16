# aws-lambda-mysql-logs-to-ess
自動生成されるやつをよしなに

# 参考URL

https://dev.classmethod.jp/cloud/aws/rds-mysql-slowquerylog-monitoring/

# eventのJSON生成方法

```
cat cloudwatch-logs.raw.json | gzip | base64 | jq -R '{awslogs:{data:.}}' > cloudwatch-logs.encoded.json
```