# System setup
The analysis was performed in Ubuntu 24.04 version of Windows Subsystem for Linux(WSL)

## Installation of Anaconda
In the terminal give the following command
```bash
wget https://repo.anaconda.com/archive/Anaconda3-2024.10-1-Linux-x86_64.sh
```
After the complete download of above folder run the folder with .sh extension as bash script with following command
```bash
./Anaconda3-2024.10-1-Linux-x86_64.sh
```
After going through all necessary steps you are ready to use the Anaconda environment

## Adding channels in Conda environment
  1) Adding Bioconda channel
      ```bash
     conda config --add channels bioconda
     ```
  3) Adding conda-forge channel
     ```bash
     conda config --add channels conda-forge
     ```
     
