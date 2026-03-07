## Development Stage Summary
This repository is currently in the planning and prototype stage.

Completed:
- thesis abstract draft
- AWS architecture design
- frontend UI prototype

Pending:
- dataset selection
- preprocessing pipeline
- model training
- backend integration
- AWS deployment

The next milestone is to finalize dataset design and run the first local modeling experiment.
# CKD AutoML Platform

An academic and engineering project for the design and implementation of an AWS-based AutoML platform for Chronic Kidney Disease (CKD) risk prediction using AutoPrognosis 2.0.

## Project Overview
This project aims to build a deployable and reproducible CKD risk prediction platform that integrates:

- structured clinical data processing
- AutoML model training with AutoPrognosis 2.0
- model artifact and registry management
- serverless inference on AWS
- a web-based user interface for clinicians or staff

The final goal of this project is not only to develop a predictive model, but also to implement an end-to-end cloud-based system that supports training, deployment, model versioning, and real-time inference.

## Current Progress
At the current stage, the following components have been completed:

- Abstract draft completed
- Core AWS platform architecture diagram completed
- Web UI prototype completed

The following components are not yet completed:

- dataset selection and acquisition
- data preprocessing
- baseline model experiments
- AutoPrognosis training pipeline
- backend API integration
- AWS backend deployment

## Research Scope
This project focuses on a standalone prototype platform for CKD risk prediction.  
At the current stage, it does **not** integrate with hospital HIS/EMR systems.

## Target Architecture
The intended AWS architecture includes:

- Route 53
- CloudFront
- S3 static website hosting
- API Gateway
- AWS Lambda for inference
- SageMaker Training Job for AutoPrognosis 2.0
- S3 data bucket and model bucket
- CloudWatch and IAM for monitoring and security

See:
- `docs/architecture/aws_architecture.md`
- `docs/architecture/完整研究架構圖.png`
<img width="2816" height="1504" alt="完整研究架構圖" src="https://github.com/user-attachments/assets/e87cffc0-40b9-42b4-9d85-cc8be776557d" />

## Repository Structure
- `docs/` thesis planning, architecture notes, dataset planning, experiment design
- `web/` web UI source code
- `backend/` future API and inference service
- `training/` future AutoPrognosis training pipeline and notebooks
- `infra/` future infrastructure-as-code or deployment specifications
- `data_schema/` schema templates and feature definitions

## Immediate Next Steps
1. Finalize dataset source and task definition
2. Create data design specification
3. Build preprocessing workflow
4. Run baseline models
5. Run AutoPrognosis 2.0 experiments
6. Define API contract between UI and backend
7. Implement local backend inference service
8. Deploy AWS backend services

## Thesis Alignment
This repository supports both:
- the master thesis writing process
- the system development and deployment process

## Notes
This repository should remain private.
Do not upload:
- real patient-identifiable data
- AWS secrets or credentials
- sensitive environment variables

Use `.env.example` or secret managers for configuration placeholders only.
