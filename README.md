# FedSGProx_GFL
This is the data result supplement for the experimental part of paper"FedSGProx: Mitigating Data Heterogeneity and Isolated Nodes in Graph Federated Learning"

## Experimental results

We evaluate the highest accuracy that different methods can achieve by executing 500 epochs in the environment of $\beta=0.8$ and $\alpha=0.5$. The experimental results of $\beta=0.8$ are as follows:

![image](https://github.com/meng1103/FedSGProx_GFL/blob/main/result/k120_ogbn-arxiv_cn1_LDA05.png) ![image](https://github.com/meng1103/FedSGProx_GFL/blob/main/result/k120_ogbn-arxiv_cn1_rate08.png)
## Scalability
we set a participation ratio of $\rho=0.5$, meaning that in each epoch, 50% of the clients are randomly selected to perform local training. The following are the accuracy results of different methods after 500 epoch iterations.

|       | **Central**  | __FedAvg__  | __FedProx__  | __FedSGProx__
|--------------|-------|------|-------|-------
|__Cora($\beta=0.8$)__   | 0.798     | 0.762    |  0.770    |   0.794   
|__Citeseer($\beta=0.8$)__   | 0.702     | 0.712    |  0.710    |   0.738   
|__OGBN-arxiv($\beta=0.8$)__     | 0.653     | 0.505    |  0.504    |   0.534   
|__Reddit($\beta=0.8$)__   | 0.942     | 0.905    |  0.904    |   0.924   



|       | **Central**  | __FedAvg__  | __FedProx__  | __FedSGProx__
|--------------|-------|------|-------|-------
|__Cora($\alpha=0.5$)__   | 0.798     | 0.760    |  0.770    |   0.786   
|__Citeseer($\alpha=0.5$)__   | 0.702     | 0.704    |  0.698    |   0.724   
|__OGBN-arxiv($\alpha=0.5$)__     | 0.653     | 0.606    |  0.608    |   0.634   
|__Reddit($\alpha=0.5$)__   | 0.942     | 0.933    |  0.933    |   0.941   


## Ablation
