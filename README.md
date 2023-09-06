# FedSGProx_GFL
This is the data result supplement for the experimental part of paper"FedSGProx: Mitigating Data Heterogeneity and Isolated Nodes in Graph Federated Learning"

## Experimental results
![image](https://github.com/meng1103/FedSGProx_GFL/blob/main/result/k120_ogbn-arxiv_cn1_LDA05.png)
## Scalability
we set a participation ratio of $\rho=0.5$, meaning that in each epoch, 50% of the clients are randomly selected to perform local training. The following are the accuracy results of different methods after 500 epoch iterations.

|       | **Central**  | __FedAvg__  | __FedProx__  | __FedSGProx__
|--------------|-------|------|-------|-------
|__Cora($\beta=0.8$)__   | 0     | 0    |  0    |   0   
|__Citeseer($\beta=0.8$)__   | 0     | 0    |  0    |   0   
|__OGBN-arxiv($\beta=0.8$)__     | 0     | 0    |  0    |   0   
|__Reddit($\beta=0.8$)__   | 0     | 0    |  0    |   0   



|       | **Central**  | __FedAvg__  | __FedProx__  | __FedSGProx__
|--------------|-------|------|-------|-------
|__Cora($\beta=0.8$)__   | 0     | 0    |  0    |   0   
|__Citeseer($\beta=0.8$)__   | 0     | 0    |  0    |   0   
|__OGBN-arxiv($\beta=0.8$)__     | 0     | 0    |  0    |   0   
|__Reddit($\beta=0.8$)__   | 0     | 0    |  0    |   0   


## Ablation
