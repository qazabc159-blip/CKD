# API Contract

## Purpose
Define the request and response schema between the web UI and backend inference service.

## Proposed Endpoint
POST /predict

## Request Example
```json
{
  "feature_1": 0,
  "feature_2": 0.0,
  "feature_3": "value"
}
