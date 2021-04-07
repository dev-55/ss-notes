# Cheat Sheet

## LocalStack

### S3
List buckets
```
    aws s3 ls --endpoint-url http://localhost:4566
```

List bucket contents
```
    aws s3 ls s3://bucket-name --endpoint-url http://localhost:4566
```

Remove bucket contents
```
    aws s3 rm s3://bucket-name --endpoint-url http://localhost:4566 --recursive
```

### SQS
List Queues
```
    aws sqs list-queues --endpoint-url http://localhost:4566
```

Read Queue
```
    aws sqs receive-message --queue-url http://localhost:4566/000000000000/QueueName.fifo --endpoint-url http://localhost:4566
```

### Logs
```
    aws logs get-log-events --log-group-name LogGroupName --log-stream-name 2021-03-25-01-00-15_48e0384eacc4_c5d45c43-2acf-43e6-84b6-f590e0c74c4d --endpoint-url http://localhost:4566

    aws logs describe-log-streams --log-group-name LogGroupName --endpoint-url http://localhost:4566

    aws logs --endpoint-url http://localhost:4566 describe-log-groups
```