# nerLTRDTA2.0
# INSTALLATION
pip or conda

# Requirements:

Python 3.7x (may work with earlier versions, not tested)

Sklearn 0.0

Numpy 1.17.0

Pandas  1.2.3

Java environment

TensorFlow

RDkit

#data
To demonstrate the superiority of the proposed model on DTA prediction in cold start scenarios, we conducted experiments to compare our approach with two state-of-the-art methods

NerLTRvsFusionDTAvsHGRLDTA/train_test_drug/*.txt---The indexes of the drugs contained in the training set and the test set respectively


# Usage
FusionDTA
HGRL-DTA
NerLTR-DTA-main

three_principles.ipynb---Three Principles for Dividing Groups

# Learning to rank
RankLib-2.16.jar(download from "https://sourceforge.net/p/lemur/wiki/RankLib/")
train:

java -jar RankLib-2.16.jar -train train.txt -ranker 0 -metric2t NDCG@50 -tree 500 -leaf 300 -shrinkage 0.03 -mls 5 -tc 256 -save t_model.txt -out t_out.txt

test:

java -jar RankLib-2.16.jar -load t_model.txt -rank test.txt -indri test_rank.txt

# Evaluation criteria
CI
MSE
Rm2

##### Note:

Some data processing is done with linux commands,the code is simple, therefore the specific code is not listed.

# Main reference
Ru X, Ye X, Sakurai T, Zou Q: NerLTR-DTA: drug–target binding affinity prediction based on neighbor relationship and learning to rank. Bioinformatics 2022, 38(7):1964-1971.
