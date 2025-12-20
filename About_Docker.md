# Docker Image Creation

*This File contains the steps needed for the installation of the Docker and creating the image of the DockerFile given to us in the task1.*

Step 1. Update the apt before installing anything (good practice)
```bash 
sudo apt-get update
```
Step 2. Install the docker.io
```bash
sudo apt-get install docker.io -y
```
Step 3. Activating the Docker service immediately
```bash
sudo systemctl start docker
```
Step 4. Configures the Docker service to start automatically every time VM boots up.
```bash
sudo systemctl enable docker
```
Step 5. Reads the Dockerfile in the current folder to create a reusable virtual image named "riscv-env" containing all the hardware tools.
```bash
docker build -t riscv-env .
```
##
## *Note - The DockerFile attached in this repository is the one that I've used for my setup, It may be different in your case.*
