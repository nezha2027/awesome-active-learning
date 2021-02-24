# Active learning summary

In this repository, previous works of active learning were categorized. 
We try to summarize the current AL works in a **problem-orientated approach** and a **technique-orientated approach**.
We also summarized the applications of AL.
The software resources and the relevant scholars are listed.

*(I can't ensure this summary covers all the representative works and ideas.
So if you have any comments and recommendations, pls let me know.)*

- [Active learning summary](#active-learning-summary)
- [At the Beginning](#at-the-beginning)
- [Problem-oriented approach](#problem-oriented-approach)
- [Technique-oriented approach](#technique-oriented-approach)
- [Practical considerations](#practical-considerations)
- [Real Applications of Active Learning](#real-applications-of-active-learning)
- [Resources:](#resources)
  - [Software Packages/Libraries](#software-packageslibraries)
  - [Tutorials](#tutorials)
- [Groups/Scholars (Not finished):](#groupsscholars-not-finished)
- [Our Subjective Opintions on AL](#our-subjective-opintions-on-al)
- [Note](#note)

# At the Beginning

Active learning is used to reduce the annotation cost in machine learning process.
It is under the assumption that some samples are more important for a given task than other samples.
There have been several surveys for this topic.
The main ideas and the scenarios are introduced in these surveys.

- Active learning: theory and applications [[2001]](https://ai.stanford.edu/~koller/Papers/Tong:2001.pdf.gz)
- **Active Learning Literature Survey (Recommend to read)**[[2009]](https://minds.wisconsin.edu/handle/1793/60660)
- A survey on instance selection for active learning [[2012]](https://link.springer.com/article/10.1007/s10115-012-0507-8)
- Active Learning: A Survey [[2014]](https://www.taylorfrancis.com/books/e/9780429102639/chapters/10.1201/b17320-27)
- Active Learning Query Strategies for Classification, Regression, and Clustering: A Survey [[2020, Journal of Computer Science and Technology]](https://link.springer.com/article/10.1007/s11390-020-9487-4)
- A Survey of Active Learning for Text Classification using Deep Neural Networks [[2020]](https://arxiv.org/pdf/2008.07267.pdf)
- A Survey of Deep Active Learning [[2020]](https://arxiv.org/pdf/2009.00236.pdf)
- ALdataset: a benchmark for pool-based active learning [[2020]](https://arxiv.org/pdf/2010.08161.pdf)
- Active Learning: Problem Settings and Recent Developments [[2020]](https://arxiv.org/pdf/2012.04225.pdf)

# Problem-oriented approach

If you are pursuing use AL to reduce the cost of annotation in a pre-defined problem setting, we summarized the previous works in a problem-oriented order.

According to scenarios and tasks, almost all the AL works could be devided into the following sub-problem settings.

|                | Pool-based                     | Stream-based         |
| -------------- | ------------------------------ | -------------------- |
| Classification | PB-classification (most works) | SB-classification    |
| Regression     | PB-regression                  | SB-regression (rare) |

Under these problem settings, there are also other dimensions：

- Batch mode (under pool-based problems)
- Additional constrains
  - Multi-class (Classification)
  - Multi-label (Classification)
  - Multi-task
  - Multi-domain
  - Multi-view/modal

Please check [here](AL_core.md) for more details.

# Technique-oriented approach

If you are trying to improve the performance of the current AL or try to find a appropriate framework for the current model, we summarized several of the previous works in a technique-orientated order.
Specifically, we care how to apply AL strategy on each type of models in this approach.

Please check [here](AL_technique.md) form more details (Not finished yet).

# Practical considerations

Besides, there are many real considerations when we implement AL to real life scenarios.
We summarize these works [here](subfields/practical_considerations.md).

# Real Applications of Active Learning

AL has already been used in many real life applications.
For many reasons, the implementations in many companies are confidential.
But we can still find many applications from several published papers and websites.

If you are wondering how could AL be applied in many other fields, we summarized a list of works [here](subfields/AL_applications.md).

# Resources:

## Software Packages/Libraries
There already are several python AL project:
- [Google's active learning playground](https://github.com/google/active-learning)
- [A modular active learning framework for Python](https://github.com/modAL-python/modAL)
- [libact: Pool-based Active Learning in Python](https://github.com/ntucllab/libact)
- [ALiPy](https://github.com/NUAA-AL/ALiPy): 
  An AL tool-box from NUAA. 
  The project is leaded by Shengjun Huang.
- [pytorch_active_learning](https://github.com/rmunro/pytorch_active_learning)
- [Deep-active-learning](https://github.com/ej0cl6/deep-active-learning)

## Tutorials
- [active-learning-workshop](https://github.com/Azure/active-learning-workshop): 
  KDD 2018 Hands-on Tutorial: Active learning and transfer learning at scale with R and Python

# Groups/Scholars (Not finished):
1. [Hsuan-Tien Lin](https://www.csie.ntu.edu.tw/~htlin/)
2. [Shengjun Huang](http://parnec.nuaa.edu.cn/huangsj/) (NUAA)
3. [Dongrui Wu](https://sites.google.com/site/drwuHUST/publications/completepubs) (Active Learning for Regression)
4. Raymond Mooney
5. [Yuchen Guo](http://ise.thss.tsinghua.edu.cn/MIG/gyc.html)

# Our Subjective Opintions on AL

Active learning has been researched over 3 decades, the fundamental theories and ideas are quite complete.
Current works are more focusing on combining AL and other research fields or looking for new applications.

In my point of view, there are several directions which are promising but not fully discovered:
- Deep active learning: from the popularity of the deep models
  - Cold start
  - Uncertainty measurement
  - Efficiently update model in AL process
- Stream based active learning: most works are about pool-based AL, but the data steam is also heavily-used in daily life. This types of works should be similar to online learning
  - Selection strategy.
- Large scale active learning: AL is invented for high labeling cost situation. However, most works are just try their algorithms on a relatively small dataset
- Practical considerations: Before utilize AL into realistic situation, there still are many technique problems
- Application scenarios

# Note

- Supervised
  - model output guided selection
  - model middle information guided selection
- Unsupervised
  - only base on the original features