# GNN Model for Anti-Money Laundering (AML)
This repository contains the GIN models needed to run the GNN for Anti-Money Laundering. For this experiment, we refer to the following two papers: [Provably Powerful Graph Neural Networks for Directed Multigraphs](https://arxiv.org/abs/2306.11586) [AAAI 2024] and [Realistic Synthetic Financial Transactions for Anti-Money Laundering Models](https://arxiv.org/abs/2306.16424) [NeurIPS 2023].

## Setup
To use the repository, you first need to install the conda environment via 
```
conda env create -f env.yml
```
Then, the data needed for the experiments can be found on [Kaggle](https://www.kaggle.com/datasets/ealtman2019/ibm-transactions-for-anti-money-laundering-aml/data). To use this data with the provided training scripts, we first perform a pre-processing step for the downloaded transaction files (e.g. `HI-Small_Trans.csv`):
```
python format_kaggle_files.py HI-Small_Trans.csv
```
The processed data will be saved in the file paths in the `data_config.json` file (Variable `aml_data`).

## Usage
To run the experiments, we run the `main.py` function and specify our model. There are two required arguments, namely `--data` and `--model`. For the `--data` argument, the folder name needs to be specified. Thus, to run the standard(simple) GNN, we use:
```
python main.py --data Small_HI --model gin
```

To train the complex GIN with edge updates, use the command:

```
python main.py --data Small_HI --model gin --emlps
```

## Result
The best model is saved in folder `bestmodel`. The test F1 score is 0.6423. The training log is saved in folder `logs`.
