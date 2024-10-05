# Follow-up Study on Sign Language Translation

👨‍🎓[Previous work](https://github.com/dancsomarci/sign-language)

## Pillars of Research & Development:

| Status | Meaning                  |
|--------|--------------------------|
| ✅     | Done                     |
| ❌     | Abandoned                |
| 🚧     | Not for now              |
| ❗      | Idea worth exploring     |


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
    - ❗Classify hands with missing points (graph vs padding representation) -> MLP vs GNN

- Continuous Fingerspelling
    - ✅Rebuild Transformer from previous study using `PyTorch`
    - Enhanced Architecture:
        - ✅Proper masking for both enc-dec inputs
        - ❗Visualize attention. Intuition suggests, that constant stream -> same token multiple times -> problem (perhaps figure out a way to enhance attention for such cases/research existing solutions)
    - ❗Improve Data handling: remove frames that don't contain detailed hand pose (+perhaps more aggressive data filtering)

### 2. 🚧 App

- Android app for data collection
- Inference (locally + Python server with streaming)
- Clean Architecture (+patterns)

### 3. 🚧 MLOps

- Azure Deployment (pipelines etc...)
- Load balancing/Job scheduling?