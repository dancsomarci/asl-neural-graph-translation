# 👨‍🎓 Follow-up Study on Sign Language Translation

This project is a continuation of my [previous work](https://github.com/dancsomarci/sign-language) on translating American Sign Language (ASL) fingerspelling using neural networks.

## 🎯 Motivation

The core idea behind this follow-up study is to **represent the human hand as a graph**—with joints as nodes and bones as edges—and apply **Graph Neural Networks (GNNs)** to recognize ASL fingerspelling. Both **Graph Convolutional Networks (GCN)** and **Graph Attention Networks (GAT)** are explored for modeling:

- **Static gestures**, where a single hand pose corresponds to a letter.
- **Dynamic sequences**, where multiple frames form a fingerspelled word.

---

## 📚 Resources

| Type      | Dataset                                                                 | Notebook                                                                 |
|-----------|-------------------------------------------------------------------------|--------------------------------------------------------------------------|
| 🖼️ Static | [TDK v2 – Static](https://www.kaggle.com/datasets/marcelldancs/tdk-v2-static)         | [`tdk-v2-static-training.ipynb`](./static_fingerspelling/tdk-v2-static-training.ipynb) |
| 🎞️ Dynamic | [TDK v2 – Sequential](https://www.kaggle.com/datasets/marcelldancs/tdk-v2-sequential) | [`tdk-v2-seq-training.ipynb`](./dynamic_fingerspelling/tdk-v2-seq-training.ipynb)     |

---

