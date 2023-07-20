## ASR and voice collector links:

This file contains a list of working links, probably more like a GIST
- 29th May, 2023
  - Code to fine-tune xlsr model: https://colab.research.google.com/drive/1kX_pBURiaujpuDYaB8O1hrLLQrK8bWsQ
  - Code to add LM: https://colab.research.google.com/drive/1AIgP6lc7BZTDrlU5yu83R05QDesWv4mw
  - Voice collector code walk: 
  - Recording by Katelyn Eng: 

## Setting up on Polaris (team local server):

### Compute for Polaris - will send user credentials via direct message on onetimesecret
server name: polaris.happyprime.io

### how do i login?
if you have a terminal you can login using ssh -p 1379 username@polaris.happyprime.io

### is there a gui to login?
yes, you can download x2go, a cross-platform client that allows remote desktop sessions : https://wiki.x2go.org/doku.php/download:start.
the only desktop environment that is supported is XFCE. Choose your screen resolution and use the details above like server name
and port number along with your usernames and passwords.

a note on directory usage and server usage

### server usage

by default sudo access is disabled. the system comes installed with cuda 11.8. the default python is 3.6.9. you can use python3.8
(which is installed on the machine) to opeate within a virtualenv. and nvidia-smi will show that there are 3x 1080Ti 12GB cards on the machine. the system is constantly 
monitored for suspcious usage, any suspicious usage or sharing of credentials will have accounts suspended. 

### directory usage

each user has a default home directory under /home/username. please do not use this directory to store large datasets. all data and code 
lives either on /home/data1 or /home/data2 these are both 3TB hard-drives each.

## Setting up on NEU Research Cluster:

## Great starting point to learn about cluster

A short 30 minutes course on LinkedIn: https://www.linkedin.com/learning/videos/introduction-to-discovery-10133140?u=74653650

Cluster website: https://rc-docs.northeastern.edu/en/latest/welcome/welcome.html

## Requesting access the cluster

- Need to request access to cluster. Only NEU students or faculty can access the cluster. It can be done by following the link: 

https://rc-docs.northeastern.edu/en/latest/first_steps/get_access.html

## 3 ways to connect to cluster

1. `Terminal`: 
ssh into the cluster using NEU username and password. Not recommended. Too tedious.

2. `Remote connection`: 
This is specific for VSCode IDE. Our team installed the remote server extension on VSCode and connected it using the NEU username and password. It is better than using the Terminal but still very slow.

3. `Accessing Open OnDemand`: **RECOMMENDED!**
Follow the link: https://rc-docs.northeastern.edu/en/latest/first_steps/connect_ood.html

Use your NEU username and password to get access into the cluster. So far, our experiments have been done using the JupyterLab Notebook. Following is the sequence of starting a notebook:

- Once logged in, go to `Interactive Apps` dropdown menu
- Choose the application, in our case: `JupyterLab Notebook`
- Setup the environment:
  - work directory: /work/van-speech-nlp/
  - partition: used gpu for our experiments, recommend all gpu's except for K40
  - CPUs: recommended between 2-4
  - Memory: preset at 4GB
  - Time: preset at 4 hours (can request upto 8 hours)
  - Need a reservation/request permission if trying to use multiple gpus
  - Can provide path to custom anaconda installed or use one of the modules on cluster, our experiments had the following custom environment: /work/van-speech-nlp/condaENV/bin
  - click launch and wait in queue to be provided access to the cluster
