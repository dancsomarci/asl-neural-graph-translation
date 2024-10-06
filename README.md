# Follow-up Study on Sign Language Translation

👨‍🎓[Previous work](https://github.com/dancsomarci/sign-language)

## Pillars of Research & Development:

| Status | Meaning                  |
|--------|--------------------------|
| ✅     | Done                     |
| ❌     | Abandoned                |
| 🚧     | Not for now              |
| ❗      | Idea worth exploring     |
| 🕐     | Only if time allows      |


### 1. 🧠 AI

- GNN Reserach
    - ✅PyTorch vs ❌Tensorflow (due to better community support)
    - ✅https://pytorch-geometric.readthedocs.io/en/latest/
    - ✅https://www.youtube.com/watch?v=8owQBFAHw7E&ab_channel=TensorFlow

    - ✅[GCN](https://www.youtube.com/watch?v=JtDgmmQ60x8&ab_channel=AntonioLonga)
    - ✅[GAT](https://www.youtube.com/watch?v=AWkPjrZshug&ab_channel=MashaanAlshammari)
    - 🚧[Point Cloud Classification](https://colab.research.google.com/drive/1D45E5bUK3gQ40YpZo65ozs7hg5l-eo_U?usp=sharing)
    - 🚧[GRNN](https://www.youtube.com/watch?v=v7TQ2DUoaBY&ab_channel=AntonioLonga)

    - ✅[PyTorch Transformer](https://www.kaggle.com/code/arunmohan003/transformer-from-scratch-using-pytorch)

- Static Fingerspelling
    - ✅Applying GNNs caused a significant bump in validation accuracy, but a decrease in test accuracy
    ![](docs/images/static_fs_results.png)
    - 🕐Classify hands with missing points (graph vs padding representation) -> MLP vs GNN

- Continuous Fingerspelling
    - ✅Rebuild Transformer from previous study using `PyTorch`
        - ✅Proper masking for both enc-dec inputs
    - ✅Enhanced Data Handling:
        - ✅Filter any special characters as this experiment focuses on traditional characters: `a-z` and `numbers`
        - ✅Identify dominant hand (enough for ASL Fingerspelling), `only work with the 21*3 coordinates of dominant hand`
        - ✅Remove frames where the dominant hand is not fully visible
        - ✅Keep sequences that have at least 3 frames/character in the target phrase
        - 🚧More professional data saving (hdf5, parquet)
        - ❗separate train-valid from test based on signer_ids
    - GNN Enhanced Architecture
        - Time Series Dataset Handling
        - GNN-based embedding
            - Deep Dive into library code: [for advanced minibatching](https://github.com/pyg-team/pytorch_geometric/blob/master/torch_geometric/loader/dataloader.py)
    - Hyperparameter opt
        - ❗Dive deeper into the concat parameter of `GATConv`
    
- Paper Related Stuff
    - ❗Real World analysis (at least measure inference time)
    - ❗🕐Use [ChicagoFSWild](https://home.ttic.edu/~klivescu/ChicagoFSWild.htm#overview) dataset
    - ❗Compare Continuous FS With Other Studies
        - [Fingerspelling PoseNet](https://arxiv.org/abs/2311.12128)
        - [Other study about comparison of approaches]()

- ❗❓🕐Cluster Analysis of Sequences
    - ❗Visualize attention. Intuition suggests, that constant stream -> same token multiple times -> problem (perhaps figure out a way to enhance attention for such cases/research existing solutions)

### 2. 🚧 App

- Android app for data collection
- Inference (locally + Python server with streaming)
- Clean Architecture (+patterns)

### 3. 🚧 MLOps

- Azure Deployment (pipelines etc...)
- Load balancing/Job scheduling?