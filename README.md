# tensorflow-speech-recognition-challenge
Repository for Kaggle Competition of Speech Recognition

## Installation for Ubuntu 16.04.3 LTS
### Install Docker CE: 
https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/

### Download the code:
    git clone https://github.com/leonardovaleriano/tensorflow-speech-recognition-challenge.git
    cd tensorflow-speech-recognition-challenge
    
### Build the Docker image:
	docker build -t tensorflow-py3-gpu .

Copy the path using pwd

### Docker run the container (Ignore the -c and argument to disable jupyter and get the terminal)
	docker run -v <path>:/app -p 8888:8888 --name tensorflow-speech-recognition-challenge -it tensorflow-py3-gpu /bin/bash -c "jupyter notebook --ip=0.0.0.0 --port=8888 --allow-root"
  
### Execute Jupyter in container
	docker start tensorflow-speech-recognition-challenge
	docker exec -it tensorflow-speech-recognition-challenge bash -c "jupyter notebook --ip=0.0.0.0 --port=8888 --allow-root"
  
### Access the Notebooks (use the token provided by Jupyter):
http://localhost:8888/
