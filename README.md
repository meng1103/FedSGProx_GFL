# FedSGProx_GFL
This is the data result supplement for the experimental part of the paper"FedSGProx: Mitigating Data Heterogeneity and Isolated Nodes in Graph Federated Learning"

## Experimental results

We evaluate the highest accuracy that different methods can achieve by executing 500 epochs in the environment of $\beta=0.8$ and $\alpha=0.5$. Among them, **Central** represents the result of centralized training. The experimental results of $\beta=0.8$ are as follows:

|       | **Central**  | __FedAvg__  | __FedProx__  | __FedSGProx__
|--------------| :-------: | :------: | :-------: | :-------: 
|__Cora($\beta=0.8$)__   | *0.798*     | 0.758    |  0.764    |   **0.792**   
|__Citeseer($\beta=0.8$)__   | *0.702*     | 0.706    |  0.728    |   **0.740**   
|__OGBN-arxiv($\beta=0.8$)__     | *0.653*     | 0.560    |  0.560    |   **0.581**  
|__Reddit($\beta=0.8$)__   | *0.942*     | 0.907    |  0.908    |   **0.931**   

<img src="https://github.com/meng1103/FedSGProx_GFL/blob/main/result/k21_cora_cn1_rate08.png" width="25%" height="25%"><img src="https://github.com/meng1103/FedSGProx_GFL/blob/main/result/k18_citeseer_cn1_rate08.png" width="25%" height="25%"><img src="https://github.com/meng1103/FedSGProx_GFL/blob/main/result/k120_ogbn-arxiv_cn1_rate08.png" width="25%" height="25%"><img src="https://github.com/meng1103/FedSGProx_GFL/blob/main/result/k123_reddit_cn1_rate08.png" width="25%" height="25%">

The experimental results of $\alpha=0.5$ are as follows:

|       | **Central**  | __FedAvg__  | __FedProx__  | __FedSGProx__
|--------------|:-------:|:------:|:-------:|:-------:
|__Cora($\alpha=0.5$)__   | *0.798*     | 0.764    |  0.780    |   **0.782**   
|__Citeseer($\alpha=0.5$)__   | *0.702*     | 0.700    |  0.696    |   **0.722**   
|__OGBN-arxiv($\alpha=0.5$)__     | *0.653*     | 0.611    |  0.612    |   **0.645**   
|__Reddit($\alpha=0.5$)__   | *0.942*     | 0.935    |  0.935    |   **0.942**  

<img src="https://github.com/meng1103/FedSGProx_GFL/blob/main/result/k21_cora_cn1_LDA05.png" width="25%" height="25%"><img src="https://github.com/meng1103/FedSGProx_GFL/blob/main/result/k18_citeseer_cn1_LDA05.png" width="25%" height="25%"><img src="https://github.com/meng1103/FedSGProx_GFL/blob/main/result/k120_ogbn-arxiv_cn1_LDA05.png" width="25%" height="25%"><img src="https://github.com/meng1103/FedSGProx_GFL/blob/main/result/k123_reddit_cn1_LDA05.png" width="25%" height="25%">

## Scalability
we set a participation ratio of $\rho=0.5$, meaning that in each epoch, 50% of the clients are randomly selected to perform local training. The following are the accuracy results of different methods after 500 epoch iterations.

|       | **Central**  | __FedAvg__  | __FedProx__  | __FedSGProx__
|--------------|:-------:|:------:|:-------:|:-------:
|__Cora($\beta=0.8$)__   | *0.798*     | 0.762    |  0.770    |   **0.794**   
|__Citeseer($\beta=0.8$)__   | *0.702*     | 0.712    |  0.710    |   **0.738**   
|__OGBN-arxiv($\beta=0.8$)__     | *0.653*     | 0.505    |  0.504    |   **0.534**   
|__Reddit($\beta=0.8$)__   | *0.942*     | 0.905    |  0.904    |   **0.924**   



|       | **Central**  | __FedAvg__  | __FedProx__  | __FedSGProx__
|--------------|:-------:|:------:|:-------:|:-------:
|__Cora($\alpha=0.5$)__   | *0.798*     | 0.760    |  0.770    |   **0.786**   
|__Citeseer($\alpha=0.5$)__   | *0.702*     | 0.704    |  0.698    |   **0.724**   
|__OGBN-arxiv($\alpha=0.5$)__     | *0.653*     | 0.606    |  0.608    |   **0.634**   
|__Reddit($\alpha=0.5$)__   | *0.942*     | 0.933    |  0.933    |   **0.941**   


## Ablation

To validate the effectiveness of the constraints and samplers, we conducted ablation studies. The initial method is FedAvg. The experimental results of incorporating constraint terms optimization without samplers are denoted as FedAvg(+constraint). The results with samplers but without constraint terms optimization are labeled as FedAvg(+sampler). Finally, FedSGProx represents the experimental results when both constraint terms and samplers are employed.

|       | __FedAvg__  | __FedAvg(+constraint)__  | __FedAvg(+sampler)__  | __FedSGProx__
|--------------| :------: | :----------------: | :----------------: | :-------:
|__Cora($\beta=0.8$)__   | 0.758    |  0.766    |  0.764    |   **0.792**   
|__Citeseer($\beta=0.8$)__   | 0.706    |  0.736    |  0.714    |   **0.740**   
|__OGBN-arxiv($\beta=0.8$)__     | 0.560    |  0.560    |  0.562    |   **0.581**   
|__Reddit($\beta=0.8$)__   | 0.907    |  0.928    |  0.909    |   **0.931**  


|       | __FedAvg__  | __FedAvg(+constraint)__  | __FedAvg(+sampler)__  | __FedSGProx__
|--------------| :------: | :----------------: | :----------------: | :-------:
|__Cora($\alpha=0.5$)__   | 0.764    |  **0.790**    |  0.768    |   0.782   
|__Citeseer($\alpha=0.5$)__   | 0.700    |  0.710    |  0.716    |   **0.722**   
|__OGBN-arxiv($\alpha=0.5$)__     | 0.611    |  0.642    |  0.609    |   **0.645**   
|__Reddit($\alpha=0.5$)__   | 0.935    |  **0.943**    |  0.937    |   0.942  


The constraints and samplers we proposed have been experimentally validated for their effectiveness, surpassing the initial FedAvg algorithm. Furthermore, combining both of them yields even better experimental results since they address different issues within Non-IID graph data.
