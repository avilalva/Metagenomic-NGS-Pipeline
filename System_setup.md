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
  2) Adding conda-forge channel
     ```bash
     conda config --add channels conda-forge
     ```

## Adding environment to conda
Since we are using two tools that is Kraken2 and trimgalore we have created two environments
1) Kraken Environment
  ```bash
 conda create -n kraken
  ```
2) Trimgalore environmnet
   ```bash
    conda create -n trimgalore
   ```

### Installing Trim Galore within "trimgalore" environment
  1. Activate the trimgalore environment
  ```bash
  conda activate trimgalore
  ```
  2. Installing the Trim Galore within environment
  ```bash
  conda install bioconda::trim-galore
  ```
  3. Deactivating the environment
  ```bash
  conda deactivate
  ```
As above will take you to base directory

### Installing Kraken2 and Kraken Biom within "kraken" environment
1. Initial step for for activation is same as above but replace "trimgalore" with "kraken"
2. Installing Kraken2 and Kraken biom within enviroment
   ```bash
   conda install bioconda::kraken2
   conda install bioconda::kraken-biom
   ```
3. Deactivation step is same as above for Trim Galore


