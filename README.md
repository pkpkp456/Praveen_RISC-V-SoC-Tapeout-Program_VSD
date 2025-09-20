# RISC-V Reference SoC Tapeout Program – VSD  

This repository documents my journey through the **RISC-V Reference SoC Tapeout Program** by VSD. It covers the end-to-end flow of RISC-V SoC design including tool setup, RTL design, verification, synthesis, and tapeout preparation.  

---

## 📖 Table of Contents  
1. [About the Program](#about-the-program)  
2. [System Requirements](#system-requirements)  
3. [Tools Installation](#tools-installation)  
   - [Resizing Ubuntu Window](#resizing-the-ubuntu-window-to-fit-screen)  
   - [Yosys](#yosys-open-source-synthesis-suite)  
   - [Icarus Verilog](#icarus-verilog-iverilog)  
   - [GTKWave](#gtkwave-waveform-viewer)  
4. [Learning Objectives](#learning-objectives)  
5. [Repository Contents](#repository-contents)  
6. [How to Use](#how-to-use)  
7. [Acknowledgments](#acknowledgments)  

---

## 📌 About the Program  
The **RISC-V Reference SoC Tapeout Program** focuses on building a strong foundation in:  
- RISC-V ISA fundamentals  
- RTL design and integration for SoCs  
- Functional verification and simulation  
- Synthesis and gate-level optimization  
- Tapeout flow for silicon realization  

This repo serves as my personal documentation of installations, lab work, scripts, and design files.  

---

## 💻 System Requirements  
To follow along, ensure you have:  
- **6 GB RAM** (minimum)  
- **50 GB HDD space**  
- **Ubuntu 20.04 or higher**  
- **4 vCPU** recommended  

---

## 🛠 Tools Installation  

### Resizing the Ubuntu Window to Fit Screen  
```bash
sudo apt update
sudo apt install build-essential dkms linux-headers-$(uname -r)
cd /media/<your-username>/VBox_GAs_7.1.8/
./autorun.sh


### Yosys (Open Source Synthesis Suite)
sudo apt-get update
git clone https://github.com/YosysHQ/yosys.git
cd yosys

# Install prerequisites
sudo apt install make build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev

# Configure and build
make config-gcc

# Initialize submodules (required for abc)
git submodule update --init --recursive

make 
sudo make install

Icarus Verilog (Iverilog)

sudo apt-get update
sudo apt-get install iverilog

GTKWave (Waveform Viewer)

sudo apt-get update
sudo apt install gtkwave


🎯 Learning Objectives

By the end of this program, I aim to:

Understand RISC-V ISA fundamentals

Gain hands-on experience in RTL design and SoC integration

Perform functional verification with open-source tools

Synthesize designs using Yosys and simulate with Icarus Verilog

Prepare designs for tapeout flow

📂 Repository Contents

Labs/ → Hands-on lab exercises

RTL/ → RTL design files

Scripts/ → Automation and helper scripts

Docs/ → Notes and reference documents

Images/ → Screenshots and installation proofs
