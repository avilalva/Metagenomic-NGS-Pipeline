# Kraken Analysis

## Reference Database Download
Here we require a reference database and you can find the reference database in this given [link](https://benlangmead.github.io/aws-indexes/k2).

Choose the database based on your computational capacity and right click on that database folder and copy the link

![Database](https://github.com/user-attachments/assets/5d227ebb-c37b-4025-96aa-dd613d429ef4)

And give this below command with the link copied to download the database folder
```bash
wget https://genome-idx.s3.amazonaws.com/kraken/k2_standard_08gb_20240904.tar.gz
```
Extract the compressed folder content to desired folder. And you are done with the database.

Keep the trimmed files and database in one folder for convenience.

## Analysis

Run this below command for files
```bash
 kraken2 --db database_folder_name --paired file1.fastq.gz file2.fastq.gz --threads int > samplekrakenoutput --report kraken_report
```
The above code withh give a kraken report as output

`-db` refers to database.

`--paired` means the given sequences are of Paired end data.

`-threads` means number of cores you would like to allocate to the process of analysis.
