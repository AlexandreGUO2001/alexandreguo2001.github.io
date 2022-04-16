# 统计方向分系介绍

## 分系时该考虑什么

|  学术兴趣 |  专业  |
|  :----:  | :----: |
|  学界的领域划分，稳定  | 每个学校的划分，变化 |
| 长期从事  | 短暂 |
| （研究生，学界/业界） | （毕业要求，排名范围）|

挖掘**学术兴趣**！以此为基础寻找导师、文献、课程等资源及决定从什么小方向毕业。

### 专业

- 数学与应用数学专业：基础、金融、概率
- 统计学专业：统计、生物统计
- 信息与计算科学专业：计算、信息
- 数据科学与大数据技术专业：大数据

### 学术兴趣（举例）

- 统计：高维统计学、生物统计、因果推断、贝叶斯统计……

- 运筹学 (operation research) ：优化、工业工程 (industrial engineering) ……

- 机器学习：深度学习（自然语言处理、计算机视觉、语音识别）、强化学习……

- 计算数学：数值PDE、计算系统生物学、计算流体力学 (computational fluid dynamics) ……

## 统计学的研究内容与价值观

统计是处理带有随机性的数据的艺术。人们设计试验并收集数据，然后希望统计学家能通过数据分析来学到一些知识，从而有助于解释和预测。统计学家致力于构建数学的理论，基于概率模型提出研究数据的方法。

> **数据 → 模型 → 算法 → 推断**

- **数据收集**：抽样调查，试验设计……（当然，大数据时代很多数据是已经帮你收集好了，现在人们已经更为关注数据分析）。

- **模型**：参数模型/非参数模型，线性/广义线性模型，神经网络，概率图模型，深度生成模型……

- *All models are wrong, but some are useful.* 学过统计以后大家会对这句话有更深的理解。统计的宗旨即是用数据和（不一定准确的）模型来认识世界。

- **算法**：凸优化，EM (Expectation-Maximization) ，MCMC (Markov Chain Monte Carlo，马尔科夫链蒙特卡洛)，VI (Variational Inference，变分推断) ……

- **推断**：从数据中得出什么信息？如数据的分布、不同变量之间的相关性与因果性等，并期望从已有的数据中预测新的数据分布。

- ***A priori v.s. A posteriori***：前者“由因及果”，如概率；后者“由果及因”，如统计。

<!-- (A priori knowledge is independent from current experience (e.g., as part of a new study). Examples include mathematics, tautologies, and deduction from pure reason. A posteriori knowledge depends on empirical evidence. Examples include most fields of science and aspects of personal knowledge.) -->

## 概率与统计的关系

引自[*All of Statistics: A Concise Course in Statistical Inference*](https://link.springer.com/book/10.1007/978-0-387-21736-9) ，Larry Wasserman著。

- Part I of the text is concerned with **probability theory**, the formal language of uncertainty which is the basis of statistical inference. The basic problem that we study in probability is:

  > Given a data generating process, what are the properties of the outcomes?

- Part II is about **statistical inference** and its close cousins, **data mining** and **machine learning**. The basic problem of statistical inference is the inverse of probability:

  > Given the outcomes, what can we say about the process that generated the data?

- 概率：若$X_t\sim\mathcal{P}$，它会有怎样的性质？

- 统计：给出数据$X_1,...,X_n\sim\mathcal{P}$，如何对这个分布$\mathcal{P}$做一些推断？

## 课程及推荐书目

课程包括各种统计/机器学习相关的课程，统计学培养方案内外均有。

1. 入门内容：概率论、数理统计。
    - 扎实的概率论基础是后续研究的关键。
    - 数理统计推荐书目：
        - 入门：
            - George Casella and Roger L. Berger, *Statistical Inference*.
            - Larry Wasserman, *All of Statistics: A Concise Course in Statistical Inference*.
        - 进阶（需了解测度论）：
            - Jun Shao, *Mathematical Statistics*.

2. 分析基础课程：实变函数、泛函分析。
    - 实变函数跟测度论重合较大，如果嫌麻烦想一步到位可以直接看Gerald B. Folland, *Reak Analysis*的前三章。
    - 统计里会用到的泛函分析最主要的是RKHS (Reproducing kernel Hilbert space，再生核Hilbert空间) ，最好还是学一下吧。

3. 理论统计进阶课程：测度论、高等概率论、高等统计学。
    - 测度论是把数理统计的内容严格讲清楚的必备工具。
    - 高等统计学相当于数理统计的测度论版本，如果先学测度论再学数理统计的话建议用Jun Shao, *Mathematical Statistics*一步到位。

4. 随机过程相关：应用随机过程、应用随机分析、随机过程论、随机分析。
    - 应用随机过程除Markov链的理论在MCMC中有用之外别的对统计价值不大（这门课随机微分方程几乎不讲）。
    - 学习SDE推荐教材：
        - Bernt Øksendal, *Stochastic Differential Equations*.
        - Weinan E, Tiejun Li, Eric Vanden-Eijnden, *Applied Stochastic Analysis*.

5. 经典统计：应用回归分析、应用多元统计分析、非参数统计、现代统计模型。

    - 前三门课适当地学一点是有必要的，但过于古典，大数据时代并非主流。虽然如此，一点都不懂也是不好的。
    - 推荐书目：
        - Toy学长的[应用多元统计分析笔记](https://zhuanlan.zhihu.com/p/91593024)和[现代统计模型笔记](https://zhuanlan.zhihu.com/p/106896222)。

6. 机器学习：机器学习基础、统计学习。

    - 这两门课算是入门课，主要介绍经典机器学习算法。
    - 推荐书目：
        - 李航，*统计学习方法*。
        - 周志华，*机器学习*。
        - Trevor Hastie, Robert Tibshirani, Jerome Friedman, *The Elements of Statistical Learning*.
    - **对机器学习感兴趣的同学，[强烈推荐贵校信科部分学生制作的这个网站](https://csdiy.wiki/) ！**

7. 理论机器学习：高维概率论、机器学习（信科）、数据科学导引、理论机器学习（信科）、高维统计学II。
    - 与上面一条区分，这些课会着重讲机器学习中的理论，重数学原理而轻上机实验。
    - 推荐书目：
        - Mehryar Mohri, Afshin Rostamizadeh, Ameet Talwalkar, *Foundations of Machine Learning*. （非常难啃，不建议入门用这本）
        - Trevor Hastie, Robert Tibshirani, Jerome Friedman, *The Elements of Statistical Learning*.
        - Shai Shalev-Shwartz, Shai Ben-David, *Understanding Machine Learning: From Theory to Algorithms*.
        - Francis Bach, *Learning Theory from First Principles*.
        - Roman Vershynin, *High-Dimensional Probability*. （高维概率论入门，无需测度论）
        - Roman van Handel, *Probability in High Dimension*. （高维概率论进阶）
        - Martin Wainwright, *High-Dimensional Statistics*.
        - Toy学长的[高等统计学II笔记](https://zhuanlan.zhihu.com/p/345935324)。

8. 贝叶斯统计、计算统计学、深度学习：统计模型与计算方法、贝叶斯理论与计算、深度生成模型（信科）。
    - 推荐书目及课程：
        - *Bayesian Data Analysis*.
        - *Deep Learning*.
        - [Stanford CS231n](http://cs231n.stanford.edu/).

9. 强化学习：强化学习（信科）、深度强化学习（信科）。

10. 优化相关：凸优化。
    - 现代机器学习、深度学习中必有对损失函数的优化，因此掌握一些基本算法及其分析而不是只会调包是很重要的。
    - 推荐书目：
        - Stephen Boyd, Lieven Vandenberghe, *Convex Optimization*.

11. 因果推断：统计和生物统计中的因果推断。

12. 生物统计相关：生物统计、计算系统生物学，以及部分生科课程。

13. 函数型数据分析。北大暂时没有相关课程，但是[姚方](https://www.math.pku.edu.cn/teachers/yaof/index.html)老师是此方面的专家。
    - 推荐书目：
        - Toy学长的[函数型数据分析笔记](https://zhuanlan.zhihu.com/p/77203545)。

14. 其他：抽样调查、试验设计。

15. 编程。
    - 现代统计研究几乎离不开编程（纯理论除外），一般的统计分析多用`R`，机器学习多用`Python`，其他的语言（如`Matlab`和`C`）不常用。
    - 按照惯例，统计系学生的码力显著弱于计算系的学生，主要还是因为统计的课大多不需要大规模写代码，而且即使要写大多数情况也是调包，很少有像数值代数、数值分析这些课一样写很底层的算法。
    - 当然，这些编程语言具体怎么用，课程上肯定不会讲，有赖于自学。一般来说入门先学个大概就行，具体细节用的时候不会再查说明。如果想实习的话，建议精通至少一门编程语言。

## 致谢

本讲稿部分内容参考了舒亦展学长在2020年做的统计学方向分系介绍以及[李通宇学长的知乎文章](https://www.zhihu.com/people/chun-cui-8-18/)，在此致谢。
