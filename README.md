# End-to-End Named Entity Recognition (NER) with BERT Transformed learning on GCP (Docker & CircleCI)

This repository implements a complete Named Entity Recognition (NER) pipeline using a pre-trained Hugging Face Transformers model (BERT). It enables to identify and classify named entities (e.g. people, organizations, locations) within text data. The pipeline leverages the power of Google Cloud Platform (GCP) for deployment and scalability, containerized with Docker for portability, and streamlined with CircleCI for continuous integration and continuous delivery (CI/CD).

# Features

- Leverages pre-trained BERT model from Hugging Face Transformers for efficient and accurate NER.
- Provides a user-friendly interface to process text data and extract named entities.
- Scales seamlessly on GCP for handling large text datasets.
- Encapsulated in Docker containers for easy deployment across various environments.
- Automated CI/CD pipeline through CircleCI for streamlined development and deployment.

# Flow Diaglram of MLops pipeline:

![MLops_NER_Architexture_Flow_Diagram](https://github.com/data-pioneer/MLops-Name-Entity-Recognition-End-to-End-main/assets/33811437/49401d27-b51e-49a8-ae71-9bfbbdb15396)


## Workflows

 - constants
 - config_entity
 - artifact_entity
 - components
 - pipeline
 - app.py

## Git commands

```bash
git add .

git commit -m "Updated"

git push origin main
```


## GCP Configuration

```bash
#Gcloud cli download link: https://cloud.google.com/sdk/docs/install#windows

gcloud init
```


## How to run?

```bash
conda create -n nerproj python=3.8 -y
```

```bash
conda activate nerproj
```

```bash
pip install -r requirements.txt
```

```bash
python app.py
```


## GCP CICD Deployment with CircleCI:

- artifact registry  --> create a repository
- change line 42,50,72,76,54 in circleci config
- Opne circleci --> create a project


### Set Environment variables in CircleCI

```bash

GCLOUD_SERVICE_KEY --> service account

GOOGLE_COMPUTE_ZONE = asia-south1

GOOGLE_PROJECT_ID

```

## Create a VM instances & setup scripts
