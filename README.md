# 本地训练初始化对联邦学习的影响研究
联邦学习是一种分布式的机器学习方式，能在保护隐私的同时协同训练全局模型。但客户端数据往往不是独立同分布的，由此引发的客户端漂移问题会严重影响模型性能。针对这个问题，本文围绕本地训练初始化提出了固定权重与可学习权重两种方法。固定权重方法通过线性加权把全局模型和历史本地模型融合在一起，其中权重为[0,1]内的固定值。可学习权重方法把融合权重当作可学习的参数，用少量本地样本来动态优化。实验结果表明，在MNIST和CIFAR-10两个数据集上，固定权重策略都表现出全局权重越高性能越好的规律，但适当保留一些本地权重，可以在不明显损失精度的前提下加快收敛。而可学习权重策略仅在本地数据上学习融合权重，导致其在两个数据集上都出现了过拟合。本文的研究结果为联邦学习中本地模型初始化策略的选取提供了实证依据。

Federated learning is a distributed machine learning approach that allows collaborative training of a global model while protecting privacy. However, client data is often not independently and identically distributed, and the resulting client drift problem can severely impact model performance. To address this issue, this thesis proposes two methods around local training initialization: fixed-weight and learnable-weight. The fixed-weight method integrates the global model and historical local model through linear weighting, with the weight set as a fixed value within [0,1]. The learnable-weight method treats the fusion weight as a learnable parameter, dynamically optimizing it with a small amount of local data. Experimental results show that on both MNIST and CIFAR-10 datasets, the fixed-weight strategy demonstrates that higher global weight leads to better performance, but appropriately retaining some local weight can accelerate convergence without significant loss of accuracy. The learnable-weight strategy, learning the fusion weight only on local data, results in overfitting on both datasets. The research results of this thesis provide empirical evidence for the selection of local model initialization strategies in federated learning.

## 在MINST和CIFAR-10两个数据集上，两种本地训练初始化方法的实验代码
固定权重实验代码：https://www.kaggle.com/code/cjwsgdtc1/cifar-10

固定权重实验代码：https://www.kaggle.com/code/cjwsgdtc1/minst

可学习权重实验代码：https://www.kaggle.com/code/starwen/cifar10

可学习权重实验代码：https://www.kaggle.com/code/starwen/minst
