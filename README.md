## ASR and voice collector links:

This file contains a list of working links, probably more like a GIST
- 29th May, 2023
  - Code to fine-tune xlsr model: https://colab.research.google.com/drive/1kX_pBURiaujpuDYaB8O1hrLLQrK8bWsQ
  - Code to add LM: https://colab.research.google.com/drive/1AIgP6lc7BZTDrlU5yu83R05QDesWv4mw
  - Voice collector code walk: 
  - Recording by Katelyn Eng: 

## Setting up on NEU Research Cluster:

## Great starting point to learn about cluster

A short 30 minutes course on LinkedIn: https://www.linkedin.com/learning/videos/introduction-to-discovery-10133140?u=74653650

Cluster website: https://rc-docs.northeastern.edu/en/latest/welcome/welcome.html

## Requesting access to the cluster

- Need to request access to cluster. Only NEU students or faculty can access the cluster. It can be done by following the link: 

https://rc-docs.northeastern.edu/en/latest/first_steps/get_access.html

## 3 ways to connect to cluster

1. `Terminal`: 
ssh into the cluster using NEU username and password. Not recommended. Too tedious.

2. `Remote connection`: 
This is specific for VSCode IDE. Our team installed the remote server extension on VSCode and connected it using the NEU username and password. It is better than using the Terminal but still very slow.

3. `Accessing Open OnDemand`: **RECOMMENDED!**
Follow the link: https://rc-docs.northeastern.edu/en/latest/first_steps/connect_ood.html

Use your NEU username and password to get access into the cluster. So far, our experiments have been done using the JupyterLab Notebook. Following are the steps to start a notebook:

- Once logged in, go to `Interactive Apps` dropdown menu
- Choose the application you wish to use, in our case: `JupyterLab Notebook`
- Setup the environment:
  - work directory: /work/van-speech-nlp/
  - partition: used gpu for our experiments, recommend all gpu's except for K40
  - CPUs: recommended between 2-4
  - Memory: preset at 4GB
  - Time: preset at 4 hours (can request upto 8 hours)
  - Need a reservation/request permission if trying to use multiple gpus or requesting more than 8 hours on the cluster
    - https://service.northeastern.edu/tech?id=sc_cat_item&sys_id=0c34d402db0b0010a37cd206ca9619b7
  - Can provide path to custom anaconda installed or use one of the modules on cluster, our experiments had the following custom environment: /work/van-speech-nlp/condaENV/bin
  - click launch and wait in queue to be provided access to the cluster
