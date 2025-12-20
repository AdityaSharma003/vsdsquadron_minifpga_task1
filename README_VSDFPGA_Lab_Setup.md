# [VSDSquadron FPGA mini](https://www.vlsisystemdesign.com/vsdsquadronfm/) Lab: Basic Message Display on RISC-V core
<div align="center">
  <img src="screenshots/outputForReadme.png" alt="RISC-V Logo" width="50%"/>
</div>

## Prerequisites
Install the following tools before proceeding:
```bash
# General dependencies
sudo apt-get install git vim autoconf automake autotools-dev curl libmpc-dev \
libmpfr-dev libgmp-dev gawk build-essential bison flex texinfo gperf libtool \
patchutils bc zlib1g-dev libexpat1-dev gtkwave picocom -y

# FPGA toolchain (Yosys/NextPNR/IceStorm)
sudo apt-get install yosys nextpnr-ice40 icestorm iverilog -y

# RISC-V Toolchain (GCC 8.3.0)
cd ~
mkdir -p riscv_toolchain && cd riscv_toolchain
wget "https://static.dev.sifive.com/dev-tools/riscv64-unknown-elf-gcc-8.3.0-2019.08.0-x86_64-linux-ubuntu14.tar.gz"
tar -xvzf riscv64-unknown-elf-gcc-*.tar.gz
echo 'export PATH=$HOME/riscv_toolchain/riscv64-unknown-elf-gcc-8.3.0-2019.08.0-x86_64-linux-ubuntu14/bin:$PATH' >> ~/.bashrc
source ~/.bashrc
 ```
---

## Setup
1. Clone the repository:
   ```bash
   cd ~
   git clone https://github.com/vsdip/vsdfpga_labs
   ```


## Checking the Installation of RISC-V toolchain
1. Review the RISC-V logo code (do not modify):
   ```bash
   cd ~/vsdfpga_labs/basicRISCV/Firmware
   nano riscv_logo.c  # Edit your name and date inside it and close (Ctrl+X)
   ```

2. Compile the program:

   ```bash
   riscv64-unknown-elf-gcc -o riscv_logo.o riscv_logo.c
   ```
3. Run it with Spike:

   ```bash
   spike pk riscv_logo.o
   ```

4.Expected output:


As I have edit it with my name and date so mine is looking like the figure shown below,
but yours will also be shown like this with your changes.

![RISC-V Logo](screenshots/outputForReadme.png)

