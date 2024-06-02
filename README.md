# End-to-end-Machine-Learning-Project-with-MLflow

## MLflow

[Documentation](https://mlflow.org/docs/latest/index.html)


##### cmd
- mlflow ui


import dagshub
dagshub.init(repo_owner='ashleshuk', repo_name='End-to-end-Machine-Learning-Project-with-MLflow', mlflow=True)

import mlflow
with mlflow.start_run():
  mlflow.log_param('parameter name', 'value')
  mlflow.log_metric('metric name', 1)

Run this to export as env variables:

```bash
export MLFLOW_TRACKING_URI=https://dagshub.com/entbappy/End-to-end-Machine-Learning-Project-with-MLflow.mlflow
export MLFLOW_TRACKING_USERNAME=entbappy 
export MLFLOW_TRACKING_PASSWORD=6824692c47a369aa6f9eac5b10041d5c8edbcef0

```