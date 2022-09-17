[![CircleCI](https://dl.circleci.com/status-badge/img/gh/Vinaba/Project4-ML/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/Vinaba/Project4-ML/tree/main)

## Project Overview

This project uses a Machine Learning Microservice API with a pre-trained `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing).

It uses a Python flask app deployed as a containerized application with Docker and [Kubernetes](https://kubernetes.io/).

### Files

* `app.py` serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.
* `requirements.txt` contains list of dependencies
* `Makefile` contains instructions for installing dependencies
* `Dockerfile` contains commands to assemble an image
* `output_txt_files` contains example Docker and Kubernetes logs from making prediction
* `.circleci` contains configuration file for automated testing environment

### Commands in use

1. Install dependencies `make install`
2. Lint check  `make lint`
3. Run standalone app:  `python app.py`
4. Run in Docker:  `./run_docker.sh`
5. Run in Kubernetes:  `./run_kubernetes.sh`
6. Sample input to make prediction:  `./make_predictions.sh`
7. Push image to Docker hub:  `./upload_docker.sh`

### kubectl commands

````
$ kubectl config view
$ kubectl get pod
$ kubectl logs <pod name>
````