# Paper-reading

## Table of Content
  - [Dataset](#Dataset-List)
  - [Autonomous Vehicle](#Autonomous-Vehicle)
  - [Contrastive Learning](#Contrastive-Learning)
  - [Continual Learning](#Continual-Learning)
  - [Trajectory Prediction](#Trajectory-Prediction)
  - [eXplainable Artificial Intelligence](#eXplainable-Artificial-Intelligence)
  - [Others](#Others)



### Dataset List
1. Argoverse:

[Paper](https://openaccess.thecvf.com/content_CVPR_2019/papers/Chang_Argoverse_3D_Tracking_and_Forecasting_With_Rich_Maps_CVPR_2019_paper.pdf)

### Autonomous Vehicle
- [Identifying Driver Behaviors using Trajectory Features for Vehicle Navigation](https://arxiv.org/pdf/1803.00881.pdf)
  - University of North Carolina at Chapel Hill
  - IROS 2018
- [Explainable Object-induced Action Decision for Autonomous Vehicles](https://arxiv.org/pdf/2003.09405.pdf)
  - University of California
  - CVPR 2020
  - Dataset: https://twizwei.github.io/bddoia_project/
  - Notes: BDD-OIA
- [Where Does the Driver Look? Top-Down-Based Saliency Detection in a Traffic Driving Environment](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=7442138)
  - University of Electronic Science and Technology of China
  - IEEE TRANSACTIONS ON INTELLIGENT TRANSPORTATION SYSTEMS


### Contrastive Learning
- [PROTOTYPICAL REPRESENTATION LEARNING FOR RELATION EXTRACTION](https://openreview.net/pdf?id=aCgLmfhIy_f)
  - ICLR 2021
  - Tsinghua University
  - Notes: As same as my idea. FUCK!
- [How Well Do Self-Supervised Models Transfer?](https://arxiv.org/pdf/2011.13377.pdf)
  - Edinburgh
  - CVPR 2021
  - Notes: they evaluate the transfer performance of 13 top self-supervised models on 40 downstream tasks, including many-shot and **few-shot** recognition, object detection, and dense prediction. They compare their performance to a supervised baseline and show that on most tasks the best self-supervised models outperform supervision, confirming the recently observed trend in the literature.
- [Momentum Contrast for Unsupervised Visual Representation Learning](https://arxiv.org/pdf/1911.05722.pdf)
  - He kaiming
  - CVPR 2020
  - Notes: MoCo, insightful figures illustrate the differences among the `memory bank`, `end to end` and `MoCo`.
- [A Simple Framework for Contrastive Learning of Visual Representations
](https://arxiv.org/pdf/2002.05709.pdf)
  - Google Brain
  - ICML 2020
  - Notes: SimCLR
- [Representation Learning with Contrastive Predictive Coding](https://arxiv.org/pdf/1807.03748.pdf)
  - Google Deepmind
  - ICLR 2020
  - Notes: CPC
- [A Theoretical Analysis of Contrastive Unsupervised Representation Learning](https://arxiv.org/pdf/1902.09229.pdf)
  - Princeton University
  - ICML 2019
  - Notes: Block Similarity
- [Contrastive Learning for Image Captioning](https://arxiv.org/pdf/1710.02534.pdf)
  - Lin Dahua
  - NIPS 2017
  - Notes: None
- [Contrastive Learning of Structured World Models](https://arxiv.org/pdf/1911.12247.pdf)
  - University of Amsterdam
  - ICLR 2020
  - Notes: **ratings 8, 8, 8**. But I don't like it. Maybe I am an idiot.

### Continual Learning
- [Meta-Learning Representations for Continual Learning](https://arxiv.org/pdf/1905.12588.pdf)
  - University of Alberta
  - NIPS 2019
  - Notes:
    - The best introduction in incremental learning I have ever seen.
    - (1) ... quickly learn prediction on new samples (2) ... avoiding overwriting older knowledge ...
    - ... sparse representations ... to leave room for future learning.
- [Task Agnostic Continual Learning via Meta Learning](https://arxiv.org/pdf/1906.05201.pdf)
  - DeepMind
  - ICML 2020
- [Online Fast Adaptation and Knowledge Accumulation (OSAKA): a New Approach to Continual Learning](https://arxiv.org/pdf/2003.05856.pdf)
  - Mila - Quebec AI Institute
  - NIPS 2020
  - Code: https://github.com/ElementAI/osaka
  - Notes: Autonomous Vehicle
- [CONTINUAL LEARNING WITH HYPERNETWORKS](https://arxiv.org/pdf/1906.00695.pdf)
  - University of Zürich and ETH Zürich
  - ICLR 2020
- [VARIATIONAL CONTINUAL LEARNING](https://arxiv.org/pdf/1710.10628.pdf)
  - University of Cambridge
  - ICLR 2018
  - Notes: Infer the change of the parameters according to the new data.
- [Riemannian Walk for Incremental Learning: Understanding Forgetting and Intransigence](https://arxiv.org/pdf/1801.10112.pdf)
  - University of Oxford
  - ECCV 2018
  - Notes: They proposed 2 evaluation metrics. They improve the EWC method. They proposed the concept of intransigence.
- [Few-Shot Class-Incremental Learning](https://arxiv.org/pdf/2004.10956.pdf)
  - Xian Jiaotong University
  - CVPR 2020
  - Code: https://github.com/xyutao/fscil
  - Notes: The code includes **cifar100**, **cub200**, **mini imagenet**.
- [Continual Learning for Named Entity Recognition](https://assets.amazon.science/65/61/ecffa8df45ad818c3f69fb1cf72b/continual-learning-for-named-entity-recognition.pdf)
  - University of Illinois at Chicago
  - AAAI 2021
  - Notes: **paper-without-code**
- [Meta-Consolidation for Continual Learning](https://arxiv.org/pdf/2010.00352.pdf)
  - Indian Institute of Technology Hyderabad
  - NIPS 2020
  - Code: https://github.com/JosephKJ/merlin
  - Reviews: https://papers.nips.cc/paper/2020/file/a5585a4d4b12277fee5cad0880611bc6-Review.html
  - Notes: Nearly same with my idea.
- Elasitic Weight Consolidation Group:
  - [Overcoming catastrophic forgetting in neural networks (EWC)](https://arxiv.org/pdf/1612.00796.pdf)
    - Deepmind
    - PNAS 2017
    - Code: https://github.com/ariseff/overcoming-catastrophic
    - Notes: EWC, **Permuted MNIST Dataset**. They use the fisher information matrix as a penalty to keep the important parameters unchanged. They give each parameter a weights that indicate how important the parameter to the old tasks. It is a kind of classical gradient Regularization method.
  - [Continual Learning Through Synaptic Intelligenc (SI)](https://arxiv.org/pdf/1703.04200.pdf)
    - Stanford University
    - ICML 2017
    - Code: https://github.com/ganguli-lab/pathint
    - Notes: SI, **MNIST Split**, **CIFAR100/CIFAR10 Split**, decouple data process code. Propose a concept: train from scratch. The perfomance is good.
  - [Memory Aware Synapses (MAS)](https://arxiv.org/pdf/1711.09601.pdf)
- [CORe50: a New Dataset and Benchmark for Continuous Object Recognition](https://arxiv.org/pdf/1705.03550.pdf)
  - University of Bologna
  - CoLR 2017
  - Code: https://vlomonaco.github.io/core50/
  - Notes: A recognition dataset for continual learning.
- [Few-Shot Incremental Learning with Continually Evolved Classifiers](https://arxiv.org/pdf/2104.03047.pdf)
  - Nanyang Technological University
  - CVPR 2021
  - Notes:
    - **Nice result analysis**.
    - few-shot incremental learning benchmark.
    - **Paper without code**.
- [DER: Dynamically Expandable Representation for Class Incremental Learning](https://arxiv.org/pdf/2103.16788.pdf)
  - ShanghaiTech University
  - CVPR 2021
  - Notes: Newest baseline but **paper-without-code**.
- [TOWARDS AI-COMPLETE QUESTION ANSWERING: A SET OF PREREQUISITE TOY TASKS](https://arxiv.org/pdf/1502.05698.pdf)
  - Facebook
  - ICLR 2016
  - Notes: Unread. Mentioned by Hung-yi Lee. A Q&A dataset that may be used for continual learning.
- [Learning without Memorizing](https://openaccess.thecvf.com/content_CVPR_2019/papers/Dhar_Learning_Without_Memorizing_CVPR_2019_paper.pdf)
  - University of Maryland
  - CVPR 2019
  - Code : https://github.com/stony-hub/learning_without_memorizing
  - Notes: Unread. Same experiment setting with `iCaRL` and their code is quite simple.
- [Learning without Forgetting](https://arxiv.org/pdf/1606.09282.pdf)
  - University of Illinois
  - ECCV 2016
  - Notes: LwF, code in matlab style. In the incremental learning period, They firstly input the new data into the old networks and record those outputs. In each training iteration, the new network should not only correctly classify the samples but also keep the output of the old part same as origin. This is like the knowledge distillation.
- [iCaRL: Incremental Classifier and Representation Learning](https://arxiv.org/pdf/1611.07725.pdf)
  - University of Oxford
  - CVPR 2017
  - Notes: `CIFAR100-B0` benchmark protocol which trains all 100 classes in several splits including 5, 10, 20, 50 incremental steps with fixed memory size of 2,000 exemplars over batches. They introduce the ProtoNet into incremental learning. Save a small set of the old data and update the old class label embeddings dynamically.
  - Related Blog : https://cloud.tencent.com/developer/article/1387877
- [Learning a Unified Classifier Incrementally via Rebalancing](https://openaccess.thecvf.com/content_CVPR_2019/papers/Hou_Learning_a_Unified_Classifier_Incrementally_via_Rebalancing_CVPR_2019_paper.pdf)
  - University of Science and Technology of China, Lin Dahua
  - CVPR 2019
  - Code: https://github.com/hshustc/CVPR19_Incremental_Learning
  - Notes: `CIFAR100-B50` benchmark protocol which starts from a model trained on 50 classes, and the remaining 50 classes are divided into splits of 2, 5, and 10 steps with 20 examples as memory per class.
- [Continual Lifelong Learning with Neural Networks:A Review](https://arxiv.org/pdf/1802.07569.pdf)
  - Hamburg University
  - NN 2019
- [A continual learning survey:Defying forgetting in classification tasks](https://arxiv.org/pdf/1909.08383.pdf)
  - KU Leuven
  - IEEE TPAMI 2020
- [Class-incremental learning:survey and performance evaluation](https://arxiv.org/pdf/2010.15277.pdf)
  - Universitat Autònoma de Barcelona
  - COLING 2020
- [Lifelong Person Re-Identification via Adaptive Knowledge Accumulation](https://arxiv.org/pdf/2103.12462.pdf)
  - Leiden University
  - CVPR 2021
  - Notes: The work inspires me.
