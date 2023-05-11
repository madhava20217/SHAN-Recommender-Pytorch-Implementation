# Sequential Recommender System based on Hierarchical Attention Network (SHAN) implementation in Pytorch

Paper citation:

Ying, Haochao, et al. "Sequential recommender system based on hierarchical attention network." IJCAI International Joint Conference on Artificial Intelligence. 2018.

Changes from the original paper:

1. The bootstrap iterations have been set as a parameter in the loss function.
2. Regularisation for weights has been removed.
3. Preprocessing: the data was generated using srdatasets, the prompts are present in the SHAN implementation notebook.

## Benchmarks

1. Gowalla dataset

| **Latent Dimensions** | **Precision@1** | **Precision@5** | **Precision@10** | **Recall@1** | **Recall@5** | **Recall@10** |
|-----------------------|-----------------|-----------------|------------------|--------------|--------------|---------------|
| **5**                 |         0.00197 |         0.00079 |          0.00092 |      0.00036 |      0.00077 |       0.00155 |
| **10**                |         0.01836 |         0.01023 |          0.00682 |      0.00348 |      0.00965 |       0.01306 |
| **20**                |          0.1082 |         0.03948 |          0.02459 |      0.02327 |      0.04088 |       0.04984 |
| **50**                |         0.44984 |         0.12472 |          0.06807 |      0.08858 |      0.12032 |       0.13117 |
| **75**                |         0.44393 |         0.14911 |             0.08 |      0.08826 |      0.14209 |       0.15189 |
| **100**               |         0.41639 |         0.14046 |          0.07482 |      0.08212 |      0.13366 |       0.14157 |

<p float="middle">
  <img src="Plots/SHAN%20Precision%20on%20Gowalla%20dataset.png" width="400" />
  <img src="Plots/SHAN%20Recall%20on%20Gowalla%20dataset.png" width="400" /> 
</p>

2. Amazon dataset

| **Latent Dimensions** | **Precision@1** | **Precision@5** | **Precision@10** | **Recall@1** | **Recall@5** | **Recall@10** |
|-----------------------|-----------------|-----------------|------------------|--------------|--------------|---------------|
| **5**                 |               0 |               0 |                0 |            0 |            0 |             0 |
| **10**                |               0 |               0 |                0 |            0 |            0 |             0 |
| **20**                |               0 |               0 |          0.00061 |            0 |            0 |       0.00061 |
| **50**                |               0 |               0 |                0 |            0 |            0 |             0 |
| **75**                |               0 |               0 |                0 |            0 |            0 |             0 |
| **100**               |               0 |               0 |                0 |            0 |            0 |             0 |

<p float="middle">
  <img src="Plots/SHAN%20Precision%20on%20Amazon-Books%20dataset.png" width="400" />
  <img src="Plots/SHAN%20Recall%20on%20Amazon-Books%20dataset.png" width="400" /> 
</p>

1. MovieLens20M dataset

| **Latent Dimensions** | **Precision@1** | **Precision@5** | **Precision@10** | **Recall@1** | **Recall@5** | **Recall@10** |
|-----------------------|-----------------|-----------------|------------------|--------------|--------------|---------------|
| **5**                 |               0 |         0.00048 |           0.0006 |            0 |      0.00024 |       0.00024 |
| **10**                |         0.00217 |         0.00135 |          0.00101 |      0.00022 |      0.00068 |       0.00101 |
| **20**                |         0.00024 |         0.00039 |          0.00056 |     2.00E-05 |      0.00019 |       0.00056 |
| **50**                |         0.00024 |         0.00092 |          0.00072 |     2.00E-05 |      0.00046 |       0.00072 |
| **75**                |               0 |         0.00087 |           0.0008 |            0 |      0.00043 |        0.0008 |
| **100**               |               0 |         0.00034 |          0.00056 |            0 |      0.00017 |       0.00056 |

<p float="middle">
  <img src="Plots/SHAN%20Precision%20on%20MovieLens20M.png" width="400" />
  <img src="Plots/SHAN%20Recall%20on%20MovieLens20M%20dataset.png" width="400" /> 
</p>
