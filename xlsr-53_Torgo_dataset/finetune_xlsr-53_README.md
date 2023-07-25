# finetuning xlsr-53 wav2vec2 model with Torgo dataset script:

This repository contains files related to running ASR training, evaluation and generating Word Error Rate for the Torgo dataset. Follow the files below to understand the whole process.

### Files inside the folder:
- `xlsr_53_fine_tune_with_Torgo_dataset.ipynb`: Colab script to finetune, evaluate and generate WER using the xlsr-53 model with the Torgo dataset
- `output_modified.csv`: csv file required for training and evaluate the performance of the xlsr-53 model

### General Guidelines:
1. The finetuning script is run on Colab and needs 2 files/folders to be uploaded to Google Drive:
    - Torgo dataset and output_modified.csv:
        - The dataset can be downloaded from the following link: http://www.cs.toronto.edu/~complingweb/data/TORGO/torgo.html
        - Go to the data section at the bottom of the page and download: `F.tar.bz2` and `M.tar.bz2` folders
        - Once downloaded, create a folder locally called `Torgo` and store the folders from the previously downloaded files (F01, F03, F04, M01, M02, M03, M04, M05)
        - Next, upload the `Torgo` folder and `output_modified.csv` file to your Google Drive
        - Once, the upload is completed, the finetuning script can be run

2. Note: To run the script, a high RAM and GPU environment is recommended. All the experiments were run using Google Colab Pro.