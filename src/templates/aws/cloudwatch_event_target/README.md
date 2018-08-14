# cloudwatch_event_target

Provides a CloudWatch Event Target resource.

## input variables

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
|account_id|The id of AWS account.|string||Yes|
|region|This is the AWS region.|string|us-east-1|Yes|
|cloudwatch_event_target_rule|The name of the rule you want to add targets to.|string||Yes|
|cloudwatch_event_target_target_id|The unique target assignment ID. If missing, will generate a random, unique id.|string|{{ name }}|No|
|cloudwatch_event_target_arn|The Amazon Resource Name (ARN) associated of the target.|string||Yes|

## output parameters

| Name | Description | Type |
|------|-------------|:----:|
|arn|The Amazon Resource Name (ARN) associated of the target.|string|
|rule|The name of the rule you want to add targets to.|string|
