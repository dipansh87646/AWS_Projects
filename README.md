# Commands
- install aws-shell
```
pip install aws-shell
```
- Configure
```
aws configure
```
- Create a collection on aws rekognition
```
aws rekognition create-collection --collection-id facerecognition_collection --region ap-south-1
```
- Create table on DynamoDB
```
aws dynamodb create-table --table-name facerecognition \
--attribute-definitions AttributeName=RekognitionId,AttributeType=S \
--key-schema AttributeName=RekognitionId,KeyType=HASH \
--provisioned-throughput ReadCapacityUnits=1,WriteCapacityUnits=1 \
--region ap-south-1
```
- Create S3 bucket
```
aws s3 mb s3://bucket-name --region ap-south-1
```
