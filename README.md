# Task-1: Environment Setup & RISC-V Reference Bring-Up

This repository contains the informartion about steps followed in the setting up of the risc-v toolchain environment for the smooth FPGA IP development.

*note:- OS used for setting up is Ubuntu (recommended) which runs on linux kernal*

## Setup of the GitHub Codespace

1. Fork the [**`vsd-riscv2`**](https://github.com/vsdip/vsd-riscv2) repository to my GitHub account as [**`vsd-riscv2_adityasharma`**](https://github.com/AdityaSharma003/vsd-riscv2_adityasharma).
2. Then create the Codespace in my repository by clicking on to Code-> Create Codespace on main branch.
3. After Codespace is succesfully built, verify the environment setup by following the **`README_RISC-V_Codespaces_noVNC.md`** file till step 3.
5. After following above 3 steps the output should looks like Figure 1.

## C code Ouput without or with changes in GitHub Codespace

<p align="center">
  <img src="screenshots/Sum1ton_Output_githubcodespace.jpeg" width="600px">
  <br>
  <b>Figure 1: Output of the c code running through spike simulator with n = 9 and n = 15 respectively as seen in the terminal.</b>
</p>

## Setting up VSDFPGA labs (RISC-V toolchain) in GitHub Codespace

1. Clone the [**`vsdfpga_labs`**](https://github.com/vsdip/vsdfpga_labs.git) repository inside the repository [**`vsd-riscv2_adityasharma`**](https://github.com/AdityaSharma003/vsd-riscv2_adityasharma) by using the bash terminal present in the Github Codespace.
2. Follow the steps present in the **`README_VSDFPGA_Lab_Setup.md`** file of the newly installed **`vsdfpga_labs`** repository.
3. After following above 2 steps the output should looks like Figure 2.

## Final Ouput:

<p align="center">
  <img src="screenshots/codespace_Ouput_Task1.png" width="600px">
  <br>
  <b>Figure 2: This contained the final output of file riscv_logo.o with the modification of "TASK 1 by Aditya Sharma dated 20 December 2025"</b>
</p>

## Setup of the noVNC GUI Desktop

1. In the Github Codespace, go to the Ports tab and follow from the step 4 mentioned in the **`README_RISC-V_Codespaces_noVNC.md`** file.
2. It is the same thing we did for the Github Codebase, just this time we'll do it on a virtual machine.
3. After following above steps the output should looks like Figure 3.

## C code Ouput without or with changes on noVNC

<p align="center">
  <img src="screenshots/Sum1ton_Output_noVNC.jpeg" width="600px">
  <br>
  <b>Figure 3: Output of the c code running through spike simulator with n = 9 and n = 15 respectively as seen in the terminal.</b>
</p>

## Setting up VSDFPGA labs (RISC-V toolchain) on noVNC 

1. Now that the initial setup of VM has been done in the above step.
2. Follow the steps present in the **`README_VSDFPGA_Lab_Setup.md`** file inside the noVNC terminal.
3. After following the above steps, output should looks like Figure 4.

## Final Ouput:

<p align="center">
  <img src="screenshots/noVNC_Ouput_Task1.png" width="600px">
  <br>
  <b>Figure 4: This contained the final output of file riscv_logo.o with the modification of "TASK 1 by Aditya Sharma dated 20 December 2025"</b>
</p>


## Setup of the Local Machine (tricky part)

1. Download Ubuntu from the official website.
2. Download the Oracle Virtual box, install it and make a VM in it. (Note:- I named my VM as VM_1).
3. Install the VS Code in it and clone all the repository locally in VM file explorer system.
4. Now install the Docker and make a Docker image using the Dockerfile provided in this repository using the steps mentioned in **`About_Docker.md`** file, according to the need (Note:- I just removed the part that i need for the noVNC setup and rest of the libraries installation was done as i will going to need them some day for this internship, and if you want to add more tools you can add on your own and then makes the image).
5. After everything is installed, follow the readme file **`README_VSDFPGA_Lab_Setup.md`** and in this running the pre-requisite part is optional as docker file already have installed them but if that fails to do so run the prerequisites part also (recommendation - run it for the double check).
6. After following the above steps, output should looks like Figure 5.

note :- if the docker file fails to install the pre-requisities, install them manually.
## Final Ouput:

<p align="center">
  <img src="screenshots/Offline_Setup_NotSOComplete.jpeg" width="600px">
  <br>
  <b>Figure 5: This contained the step just above the final output of file riscv_logo.o for the local setted up VM"</b>
</p>

##

*Note:- I am getting issue while downloading spike in the local setup with the docker and without the docker that's why not getting the final output, hence working on it.
Once I'll figure that out in the offline setup will attach here.

Yay, now we have setup a clean working environment for the FPGA development purposes for the Git CodeSpace and noVNC.
