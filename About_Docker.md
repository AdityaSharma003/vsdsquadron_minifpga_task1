# Docker Image Creation

*This File contains the steps needed for the installation of the Docker and creating the image of the DockerFile given to us in the task1.*

Step 1a. Update the apt before installing anything (good practice)
```bash 
sudo apt-get update
```
Step 1b. Upgrade the apt before installing anything (good practice)
```bash 
sudo apt upgrade
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
Step 5a. Reads the Dockerfile in the current folder to create a reusable virtual image named "riscv-env" containing all the hardware tools.
```bash
sudo docker build -t riscv-env .
```
Step 5b. Run the container and save the name of the container.
```bash
sudo docker run -it -v ~/<working_directory>:/work my_riscv_env
```
Step 6. Make the container gets open everytime you'll open the terminal (note:- after opening terminal, now it will ask for the password).
```bash
sudo docker run -d --name my_riscv_container -v $(pwd):/work my_riscv_env tail -f /dev/null
```
Step 7. Edit the .bashrc file.
```bash
cd ~
nano ~/.bashrc
```
Scroll to the bottom and paste these lines at the bottom of the file and save the file:
```bash
sudo docker start my_riscv_container > /dev/null 2>&1
sudo docker exec -it my_riscv_container /bin/bash
```
Step 8. Close the terminal and reopen it, then you'll see -> **`root@<random_number>:/work# `**. If yes then you have the correct setup to move on and if not check for the discrepency at your end.
##
## *Note - The DockerFile attached in this repository is the one that I've used for my setup, It may be different in your case.*
