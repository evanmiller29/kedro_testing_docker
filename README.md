# kedro_testing_docker

This Docker file is used to execute the Kedro development tests on whichever machine you develop on.
The process is as follows:

1. Place Kedro code you're developing in the Kedro folder
2. Copy requirements.txt and test_requirements.txt into the base directory
2. Build the docker image from your docker file ```docker build -t kedro_dev .```
3. Then either use ```docker-compose``` to spin up the image and mount the kedro folder
4. CD into the active kedro image using ```docker exec -it kedro_dev_testing_kedro_1 /bin/bash``` and navigate to the kedro folder
5. Execute ```make lint``` and ```make tests```