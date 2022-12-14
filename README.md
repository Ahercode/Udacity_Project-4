[![CircleCI](https://dl.circleci.com/status-badge/img/gh/Ahercode/Udacity_Project-4/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/Ahercode/Udacity_Project-4/tree/main)


## Project Overview

In this project, I made use of the skills I have acquired in this course to operationalize a Machine Learning Microservice API. 

Having been given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests my ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

My project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project I:
* Test my project code using linting
* Complete a Dockerfile to containerize this application
* Deploy my containerized application using Docker and made a prediction
* Improve the log statements in the source code for the application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and made a prediction
* Uploaded a this repo with CircleCI to indicate that my code has been tested and passed.

You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

**The final implementation of the project will showcase your abilities to operationalize production microservices.**

---

## Setup the Environment

* Create a virtualenv with Python 3.7 and activate it. Refer to this link for help on specifying the Python version in the virtualenv. 
```bash
python3 -m pip install --user virtualenv
# You should have Python 3.7 available in your host. 
# Check the Python path using `which python3`
# Use a command similar to this one:
python3 -m virtualenv --python=<path-to-Python3.7> .devops
source .devops/bin/activate
```
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
### files in the repository
* `.circleci` directory contain the .circleci `config.yml` file
* `model_data` directory contains the csv data
* `output_txt_files` directory contains the `docker_out.txt` && `kubernetes_out.txt`
* `app.py` is the python file dfining the application
* `Dockerfile` is the Dockerfile
* `requirement.txt` contains the python requirement for the `app.py`
* `run_docker.sh` contains the script to build and run docker locally
* `run_kubernetes.sh` contains to orchestrate kubernetes from the docker image
* `upload_docker.sh` contains the script to upload the docker image to dockerhub
* `Makefile` The Makefile includes instructions on environment setup and lint test
* `make_predictions.sh` for making predictions 

