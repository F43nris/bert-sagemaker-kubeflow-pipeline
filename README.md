# bert-sagemaker-kubeflow-pipeline
This project demonstrates an end-to-end Machine Learning Operations (MLOps) pipeline using Kubeflow and AWS SageMaker. The pipeline includes data preprocessing, model training, and deployment stages, utilizing the BERT model for sentiment analysis on product reviews. 

## Project Structure

The project is structured as follows:

- `code/`: Contains the Python scripts for the pipeline.
- `hyper-parameter-tuning/`: Contains scripts for hyperparameter tuning (currently not used in the pipeline).
- `create_bert_sagemaker_kubeflow_pipeline.ipynb`: Jupyter notebook that contains the code for setting up and running the pipeline.

## Pipeline Overview

The pipeline consists of three main stages:

1. **Feature Engineering**: Preprocesses the raw data into a format that can be used for training the model.
2. **Training**: Trains the BERT model using the preprocessed data.
3. **Deployment**: Deploys the trained model to a SageMaker endpoint for inference.

## Setup

### Dependencies

The project requires the following dependencies:

- SageMaker Python SDK
- Kubeflow Pipelines SDK
- AWS CLI

These can be installed using pip:

```bash
pip install sagemaker==1.72.0
pip install https://storage.googleapis.com/ml-pipeline/release/0.1.29/kfp.tar.gz --upgrade
pip install awscli==1.18.140
```

### Environment Variables

The pipeline requires several environment variables to be set, including the AWS region, account ID, S3 bucket name, and IAM role. These are set in the Jupyter notebook.
