# Trimming
After Quality check of FastQC the trimming of adaptars has to be performed and here we use Trim Galore for trimming. 

### Procedure:

1. Open directory where your fastq files are present
2. Activate the conda environment for trimgalore
   ```bash
   conda activate trimgalore
   ```
3. I had two paired end data so the commands were
   ```bash
   trim_galore --paired file1.fastq.gz file2.fastq.gz -o trimmed -q 8
   ```
   Where in above command we say is for a data that is paried `--paired` followed by mentioning the file names and then we mention the out put directory where the files are been saved. In our case the output `-o` was in folder named "trimmed" . `-q` is for quality trimming with score of `8`.
   
   **<ins>Note: </ins>** If quality is not set then there will be a default quality of 20 will be set

   The trimmed files will be stored in a folder named "trimmed" and then you can perfor fastqc analysis to check the quality after trimming for the samples.
