# AWS Target Architecture

## Region
ap-northeast-1

## Components
- Route 53
- CloudFront
- S3 static website hosting
- API Gateway
- Lambda inference
- SageMaker Training Job
- EC2 backup training environment
- S3 data bucket
- S3 model bucket
- CloudWatch
- IAM

## Design Intent
- web UI separated from backend
- training separated from inference
- model artifacts centrally stored in S3
- inference always uses the latest registered model
- system supports future retraining and lightweight deployment updates
