# Internet2 IAM Online February 2025

This project is meant to demonstrate how LLM's can be run on a local machine using ollama, a simple AI powered app using the python langchain framework, and how prompt injection can be used to override access controls implemented during training. 

## Prerequisites
- Docker and Docker Compose
- VSCode and the VSCode Devcontainers extension *optional*

## How to run
1. Clone this project and then from the project's root folder execute the command `docker compose build` or `docker-compose build` to build the contained docker images for ollama and the python ai app.
2. In the same terminal window execute the command `docker compose up -d` or `docker-compose up -d` to start the application stack in the background.
3. Either:
3a. Open the project in VSCode then select to open the folder in a Devcontainer
3b. Or in the earlier terminal window execute the command `docker exec -it internet2-iam-online-2025-python-app-1 bash` to mount the container's bash terminal
4. The containers working directory will be `/repo` which is a mount of this live project folder (meaning changes you make here will be seen when you try to run them in the container).
5. To run the python app navigate to the `app` directory then run `python main.py` (depending on your machine startup may take a minute or so)
6. To exit the python app enter `ctrl + C` and to exit the container enter `exit` followed by `docker compose down` or `docker-compose down` to stop the application stack

## Other info
- The ollama container provided in this project is based on the offical ollama docker container found here: https://hub.docker.com/r/ollama/ollama
- The ollama container may also be directly mounted and contains a copy of the DeepSeek-R1:1.5b model.
- Link to the VSCode DevContainers extension: https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers

#### Any questions or issues related to this project can be sent to zac@instrumentalid.com and I will try to address them as I find time. This project is for educational purposes only and not intended for production usage or malicious intent. 