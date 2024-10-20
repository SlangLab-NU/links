## AAC application document link:
  - Latest Draft: September 12, 2023: <a href="https://docs.google.com/document/d/1dXDzyCJ8A2fEvlQfw6xwGMRTD8q0EAvBN9bEAdGkNO0/edit?usp=sharing" target="_blank">AAC Google Doc</a>

## PSST with LM
- [Lauryn's LM notebook](https://colab.research.google.com/drive/1gGITlubcQFnzsnLj4SlOa_KN0qL7MY5u?usp=sharing)
## ASR and voice collector links:

This file contains a list of working links, probably more like a GIST:
  - Code to fine-tune xlsr model: 
    - May 29, 2023: <a href="https://colab.research.google.com/drive/1kX_pBURiaujpuDYaB8O1hrLLQrK8bWsQ" target="_blank">Version 1</a>
    - July 24, 2023: <a href="https://colab.research.google.com/drive/12D3XOoNT610DyrQQPBsGcZQh1LVJA7YO?usp=sharing" target="_blank">Version 2</a>
    - September 14, 2023 (latest version): <a href="https://colab.research.google.com/drive/1J2UVEQNWdZZy7Z6ZDafFUksLbNI0hjfG?usp=sharing" target="_blank">Version 3</a>
  - Code to add LM: <a href="https://colab.research.google.com/drive/1AIgP6lc7BZTDrlU5yu83R05QDesWv4mw?usp=sharing" target="_blank">LM Google Colab</a>
  - Voice collector code walk:
  - Recording by Katelyn Eng: <a href="https://drive.google.com/file/d/1pwbsO7L9rY88peNSeNPOdjYzmtJoAV2R/view?usp=sharing" target="_blank">Recording</a>
  - Prompts for VoiceCollector: <a href="https://docs.google.com/document/d/1WOhUgN8w8LyG6c0FX0olAUzpQkTmwm-E_Wg71Eb4WyQ/edit?usp=sharing" target="_blank">Voice Collector Google Doc</a>
  - KenLM Language Model Integration with Torgo dataset (fine-tuned from xlsr model):
    - [Build n-gram language model with KenLM](https://colab.research.google.com/drive/1s6qAjX3A55ezwS2oAh0MoRvYp7CLd68o?usp=sharing)
    - [Fine-turning wav2Vvec2 model with Torgo](https://colab.research.google.com/drive/19zJW6BBOE1NMuBduCE7V_Z07jcSJT3RL?usp=sharing)
    - [n-gram LM integration](https://colab.research.google.com/drive/1HU362QyYfRKxnVP-1J5aTZ19BEXcGa5r?usp=sharing)

## Setting up on NEU research cluster:

## Great starting point to learn about cluster

A short 30 minutes course on LinkedIn: <a href="https://www.linkedin.com/learning/videos/introduction-to-discovery-10133140?u=74653650" target="_blank">Tutorial</a>

Cluster website: <a href="https://rc-docs.northeastern.edu/en/latest/welcome/welcome.html" target="_blank">Website Link</a>

## Requesting access to the cluster

- Need to request access to cluster. Only NEU students or faculty can access the cluster.
- It can be done by following the link: <a href="https://rc-docs.northeastern.edu/en/latest/first_steps/get_access.html" target="_blank">Access Link</a>

## 3 ways to connect to cluster

1. `Terminal`: 
ssh into the cluster using NEU username and password. Not recommended. Too tedious.

2. `Remote connection`: 
This is specific for VSCode IDE. Our team installed the remote server extension on VSCode and connected it using the NEU username and password. It is better than using the Terminal but still very slow.

3. `Accessing Open OnDemand`: **RECOMMENDED!**
Follow the link: <a href="https://rc-docs.northeastern.edu/en/latest/first_steps/connect_ood.html" target="_blank">Access Link</a>

Use your NEU username and password to get access into the cluster. So far, our experiments have been done using the JupyterLab Notebook. Following are the steps to start a notebook:

- Once logged in, go to `Interactive Apps` dropdown menu
- Choose the application you wish to use, in our case: `JupyterLab Notebook`
- Setup the environment:
  - Work directory: /work/van-speech-nlp/
  - partition: used gpu for our experiments, recommend all gpu's except for K40
  - CPUs: recommended between 2-4
  - Memory: preset at 4GB
  - Time: preset at 4 hours (can request upto 8 hours)
  - Need a reservation/request permission if trying to use multiple gpus or requesting more than 8 hours on the cluster: <a href="https://service.northeastern.edu/tech?id=sc_cat_item&sys_id=0c34d402db0b0010a37cd206ca9619b7" target="_blank">Reservation Request</a>
  - Can provide path to custom anaconda installed or use one of the modules on cluster, our experiments had the following custom environment: /work/van-speech-nlp/condaENV/bin
  - Click launch and wait in queue to be provided access to the cluster
