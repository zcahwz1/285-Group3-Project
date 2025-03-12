# Graph-Based Deep Learning for AML Detection: GNNs and DeepSeek-Enhanced PPO.
## Introduction
Money laundering (AML) poses significant challenges to financial security. Traditional rule-based AML detection systems struggle to identify complex laundering patterns. Recent advances in Graph Neural Networks (GNNs) and Reinforcement Learning (RL) provide promising solutions for dynamic transaction analysis.  
This project leverages AMLworld's GNN model and integrates a DeepSeek-enhanced Proximal Policy Optimization (PPO) model to improve AML detection. DeepSeek scores are used as a reward function in the RL framework to refine transaction classification.  

## Methodology
### GNN Model using AMLworld
Graph-based learning using GIN, edge update, and Reverse Message Passing. See the folder GNN_Model.

### DeepSeek-Reward PPO Model
See the folder RL_Model.

### Dataset
The data set can be downloaded on Kaggle. Here is the Link:
https://www.kaggle.com/datasets/ealtman2019/ibm-transactions-for-anti-money-laundering-aml/data

## Usage
 Please see the README files in the two models' folders.
