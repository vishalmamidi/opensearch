# opensearch

## Alerting on OpenSearch

https://docs.aws.amazon.com/opensearch-service/latest/developerguide/alerting.html

### Amazon SNS 
##### IAM ROLE

Trust Relationship
```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Principal": {
                "Service": "es.amazonaws.com"
            },
            "Action": "sts:AssumeRole"
        }
    ]
}
```
Permission 
```
AmazonSNSFullAcces
```

##### service account
```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": "sts:AssumeRole",
            "Resource": "arn:aws:iam::<ACCOUNT-ID>:role/<ROLE-NAME>"
        }
    ]
}
```
