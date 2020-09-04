
# Medico automatic polyp segmentation challenge
This repository aims to provide a skeleton for preparing your submission to the [Medico automatic polyp segmentation challenge](https://multimediaeval.github.io/editions/2020/tasks/medico/).


We thank you for participating in the "Medico automatic polyp segmentation challenge" and wish you the best of luck.

## How to Participate

We offer two tasks, 1. Polyp Segmentation task (required), and 2. Alogorithm efficiency task (required). 

## Task 1. Polyp Segmentation task (required)
For the task 1, please submit the prediction masks in a zip file. 

## Task 2. Alogorithm efficiency task (required)
For, task 2, please submit the docker image. 

For starters, we require that each submission is delivered in the form of a Docker image. This Docker image should create the submission file described in the challenge description. If you are new to docker, a good place to start is the [Get Started](https://docs.docker.com/get-started/) page of the official Docker documentation.


To participate, we require you to build a Docker image of your submission which includes all required dependencies and can be run using the latest version of Docker. Please note that the data should not be included within the Docker image itself, as it will be injected by us. Assume that the test dataset will be located at `/biomedia`. An example submission is included within this repository, where we show an example of a Keras based submission.

## Testing your Docker image
To test you submission, run the following bash command:

```bash
sudo docker run -v <test_set_location>:/biomedia -a stdin -a stdout -a stderr <docker_id> > biomedia_submission.txt 
```

The results should be a `.txt` file in the format of the example shown in the file `example_biomedia_submission.txt` located within this repository.

## Submitting your Docker Image

To submit your Docker image, we recommend that you export it using the following bash command:

```bash
sudo docker save <docker_id> > biomedia_image.tar
```

This command will produce a tar file of your Docker image which can easily be sent to one of the organizers of Biomedia 2019. Once the Docker image is exported, submit it to one of the following email addresses; debesh@simula.no, or steven@simula.no.

For any questions, feel free to contact debesh@simula.no or steven@simula.no.
