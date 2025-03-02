# MEDIRL
This repository implements the method described in the paper **"Modeling Human-like Driving Behavior Based on Maximum Entropy Deep Inverse Reinforcement Learning"**. The repository provides an implementation of Maximum Entropy Deep Inverse Reinforcement Learning (MEDIRL) for modeling human-like driving behaviors based on naturalistic driving data.

**Modeling Human-like Driving Behavior Based on Maximum Entropy Deep Inverse Reinforcement Learning**  
[Jiamin Shi](https://example.com), [Tangyike Zhang](https://example.com), [Shitao Chen](https://example.com), [Nanning Zheng](https://example.com), [Jingmin Xin](https://example.com)  
[National Key Laboratory of Human-Machine Hybrid Augmented Intelligence, National Engineering Research Center for Visual Information and Applications, Institute of Artificial Intelligence and Robotics, Xi'an Jiaotong University](http://example.com)  
**[[Paper]](https://ieeexplore.ieee.org/document/xxxxxxx)** &nbsp; **[[arXiv]](https://arxiv.org/abs/xxxxxxxx)**

## Table of Contents
1. [Introduction](#introduction)
2. [Getting Started](#getting-started)
3. [Usage](#usage)
4. [References](#references)
5. [License](#license)

## Introduction
Modeling expert driving behavior is crucial for the successful implementation of human-like autonomous driving. In this paper, we propose a new sampling-based Maximum Entropy Deep Inverse Reinforcement Learning (MEDIRL) framework. This framework leverages naturalistic human driving data to train the reward model and evaluates driving behaviors by the reward of sampled candidate trajectories. The proposed method uses deep neural networks to learn the feature-reward mapping, offering superior fitting capabilities over traditional linear reward functions. We introduce two trajectory samplers: one for long-term decision-making and one for short-term planning, which simplify the partition function calculation in the MEDIRL algorithm. Our approach also provides a solution to the probability estimation of driving behaviors by calculating the likelihood of sampled trajectories based on their reward values. We conduct comparative experiments on the NGSIM US-101 Highway dataset, and the results demonstrate the superiority of our model in personalizing reward functions and its applicability to modeling driving behaviors across various time horizons.

## Getting Started
To get started with the project, follow the steps below:

### Install Dependencies
First, install the necessary dependencies:
```shell
pip install -r requirements.txt
Download the NGSIM Dataset
Download the NGSIM dataset from this website and export it as a CSV file. Once downloaded, run the dump_data.py script with the path to the CSV file:

shell
复制代码
python dump_data.py [YOUR PATH]/Next_Generation_Simulation__NGSIM__Vehicle_Trajectories_and_Supporting_Data.csv
(Note: This step may take some time depending on the size of the dataset.)

Usage
After setting up the environment, you can run the IRL for either personalized or general cases. To run the IRL for personalized behavior:

shell
复制代码
python personal_IRL.py
To run for a general case:

shell
复制代码
python general_IRL.py
References
If you find this repository useful for your research, please consider citing our work:

bibtex
复制代码
@article{shi2023modeling,
  title={Modeling Human-like Driving Behavior Based on Maximum Entropy Deep Inverse Reinforcement Learning},
  author={Shi, Jiamin and Zhang, Tangyike and Chen, Shitao and Zheng, Nanning and Xin, Jingmin},
  journal={IEEE Robotics and Automation Letters},
  year={2023},
  publisher={IEEE}
}
License
This project is released under the MIT License. The NGSIM data processing code is borrowed from NGSIM interface, and the NGSIM environment is built on top of highway-env, which is also released under the MIT license.
