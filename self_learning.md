<head>
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
    <script type="text/x-mathjax-config">
        MathJax.Hub.Config({
            tex2jax: {
            skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
            inlineMath: [['$','$']]
            }
        });
    </script>
</head>


# 北大数院统计、机器学习方向自学指南

<!-- As an undergraduate student, you can never underestimate how indispensable **self-learning** is. Because attending the classes, especially in PKU, may not always be the most efficacious way to master the knowledge and help you do well in exams. And I am more than upset to see that, in School of Mathematical Sciences of PKU, the teaching quality of many courses has ample room for improvement. Many courses, such as *Abstract Algebra* and *Mathematical Statistics*, still use out-dated textbooks, such as the so-called “little yellow books” published by PKU publishing house decades ago, that are not only badly composed – few is edited by LaTeX and the font is ugly, but also unintelligible and incomprehensible. Consequently, those books seriously puncture students’ interest of the knowledge and deter us from learning efficiently and happily, not to mention laying a solid foundation for the future study. And besides, some of the teachers, deficient of the ardor of teaching and even the sense of responsibility, teach lectures in a way that transforms learning into a torture.  -->

<!-- In this website, I would like to share some of my self-learning experiences in some courses of mathematics, statistics and data sciences. I would like to share with you, with utter cordiality, the books and online courses I have found and taken use of, hoping that this can make you learn more efficiently. I strongly believe that, ***there is no stupid student, but bad teachers and inappropriate methods***. -->

此项目灵感来源于 <https://csdiy.wiki/> 。我希望借此总结经验，同时给后人提供一些选课和学习上的指导。

所有内容仅代表个人观点，欢迎向我提供意见和建议！

## 推荐的选课顺序及高年级课程先修关系综述

### 官方培养方案（全院必修课）

- 一上：数学分析I，高等代数I，解析几何，计算概论（B）
- 一下：数学分析II，高等代数II，数据结构与算法（B）
- 二上：数学分析III，抽象代数，[概率论]
- 二下：常微分方程，复变函数，概率论，数学模型/应用数学导论/机器学习基础，[数理统计]，[应用随机过程]

注：**具体培养方案以当年官方公布的培养方案为准，此处仅供参考。**2021年秋季学期起概率论每学期均开，2022年春季学期起数理统计和应用随机过程每学期均开（这两门课并非全院必修课，只是统计方向的必修课，故也列在此处）。**某些方向**数学模型/应用数学导论/机器学习基础可相互替换，具体见培养方案。

### 提前选课需要掌握的先修知识

- 概率论：先修知识为数分高代，需要掌握多元函数的求导和积分（会算即可），不要求掌握曲线积分、曲面积分、含参变量积分。
- 实变函数：官方培养方案为三上课程。可在二上与数学分析III同时学习。数学分析III由于缺乏点集拓扑的工具，多元Riemann积分定义比较麻烦且无法严谨表示，而实变函数的Lebesgue积分理论提供了一元函数和多元函数积分的统一框架，定义严谨且漂亮。因此，实变的学习并不需要以数分III多元Riemann积分为前置知识，但数分III里面偏导数的概念是需要的。
- 测度论：官方培养方案为三下课程。由于测度论和实变的内容重合度较大，学过实变再学测度论会相对简单，当然没有学过实变也不影响。除非天赋异禀，不建议跳过初等概率论直接学测度论和高等概率论。
- 泛函分析：官方培养方案为三下课程。如二上学过实变，可在二下学习。泛函分析是否需要实变作为前置知识取决于授课教师，有的老师会回避实变的内容（如举例子时用$\ell^p$空间代替$L^p$空间），也有的老师甚至默认学生了解基本的测度论知识（包括一般测度空间$(X,\mathcal{F},\mu)$的定义，会讲Radon-Nikodym导数等）。因此如果没有学过实变（包括自学），不建议修泛函。此外泛函在举例子的时候可能会稍微涉及一些偏微分方程和复变的知识，但无关紧要。泛函不是统计方向的选修课程，在比较初等的统计中较少用到，但在理论机器学习中很可能用到，因此建议统计方向的学生还是需要学一下，但可以不用急着二下就学。
- 数理统计：官方培养方案为三上课程。先修知识为概率论，除非概率论提前预习过且熟练掌握，不建议和概率论同步学习。如果有测度论基础则更好。
- 应用随机过程：官方培养方案为三上课程。先修知识为概率论。本课程讲授Markov链、跳过程和Brown运动，尽量回避测度论知识。
- 偏微分方程：官方培养方案为三上课程。先修知识为数分高代和常微分方程，无需实变和泛函基础（如果学过更好），但对数分III的多元微积分（包括曲线积分、曲面积分）要求较高，因此不建议与数分III同时学习。偏微分方程不是统计方向的选修课程，但在机器学习中可能会用到，统计方向的学生可根据自身情况选择是否学习。

以下三门均为计算方向的必修课，前两门本人没有选过，对课程内容的理解并不是很深刻，不敢多做评价，仅供参考。计算系的课程一般都用MATLAB或C/C++作为上机作业的编程语言，Python因为运算速度问题较少用，因此建议选课前了解一下MATLAB的基本使用方法。学校门户提供正版MATLAB软件的下载渠道，如果嫌下载安装麻烦可以用开源编程语言[GNU Octave](https://octave.org/index)，语法基本与MATLAB相同，仅包含MATLAB的基础功能（本科课程完全够用）。

- 数值代数：官方培养方案为三上课程。先修知识为数分I、II和高代，如果大一结束后明确打算做计算数学方向可提前到二上选。
- 数值分析：官方培养方案为三下课程。先修知识为数分高代，需要对概率论有所了解（涉及MCMC算法）。个人感觉数值分析难度低于数值代数，如打算做计算数学方向且二下时间充足可二下选课。
- 最优化方法：2022-2023学年之前为春季学期课程，另有一门课程“凸优化”秋季学期由文再文老师开；2022年秋季学期起两门课合并至秋季学期的“最优化方法”，由[文再文老师](https://bicmr.pku.edu.cn/~wenzw/)授课。先修知识为数分高代，稍微涉及一些概率论，要求熟练掌握向量和矩阵函数的导数（这些数分III不会细讲，参考：Kaare Brandt Petersen, and Michael Syskind Pedersen. [*The matrix cookbook*](https://ece.uwaterloo.ca/~ece602/MISC/matrixcookbook.pdf). Technical University of Denmark 7.15 (2008): 510.）。

此外，应用数学导论（官方培养方案为二下课程）基本是数值代数和数值分析各选一些内容进行授课，重合度较高。

### 要不要提前选课？

从2020级起提前选课的学生人数剧增，**强烈反对盲目跟风提前选课**！

一上基本没有人会提前选课，除非入学前已经预习。经过一个学期的学习，你应该对自己的学习水平和课程压力有所了解。请思考这几个问题：

1. 你的学习能力是否足够提前修高年级课程了？新增加的课有没有充足的时间用来学习？如果修官方培养方案的课程压力已经很大了，平时没有多余的时间，那么不建议提前选课！
2. 提前选课需要的先修知识有没有熟练掌握？例如，如果多元微积分都算不熟练，就不要提前选概率论了。
3. 是否有把握提前选课拿到较好的分数（85及以上，即“优秀”）？如果晚一年选，等先修知识都掌握扎实了，也许会有更高的分数。如果不在意绩点，那随意。
4. 提前选课是为了早日找到自己感兴趣的方向、早日开始科研，还是看别人提前选自己也想提前选？提前选课不等于学习能力强，选课多并不是值得炫耀的事情。

是否需要选**实验班**同理。如果你对这门课感兴趣且有信心能学好，这门课对你今后的研究方向也有用，那么选实验班是一个很好的选择。至于分数，虽然实验班考试会比较难但是老师一般会调分，优秀率通常会达到60%（普通班优秀率至多40%）；此外，2019级起实验班成绩在保研分数计算时会乘1.05倍（具体见数院门户的官方保研细则，此处仅供参考），所以如果学习水平过硬不用太担心实验班的给分问题。

## 英文阅读和写作能力

英文为全球通用的数学学术语言。

## 基础课：数学分析、高等代数、概率论、数理统计

**数学分析**

官方教材：伍胜健. *数学分析（全三册）*. 北京大学出版社, 2009.

习题集：谢惠民, 恽自求, 易法槐, and 钱定边. *数学分析习题课讲义（全两册）*. 高等教育出版社, 2018.

**高等代数**

官方教材：

1. 丘维声. *高等代数（全两册）*. 高等教育出版社, 20??.
2. 见[安金鹏老师高等代数实验班课程主页](https://www.math.pku.edu.cn/teachers/anjp/algebra)。

**概率论**

官方教材：李贤平. 概率论基础.  高等教育出版社, 2010.

习题集：David Stirzaker. *One thousand exercises in probability*. Oxford University Press, USA, 2020.

诚如[陈大岳老师所言](https://www.math.pku.edu.cn/teachers/dayue/Homepage/prob.htm)，李贤平课本是目前中文概率论教科书中最完善的一本，用此书及配套习题集（全为课本习题详细解析）自学不难。注意概率论课程中不介绍大数定律及中心极限定理的严格证明，这些内容会在学完测度论之后在高等概率论课程中用测度论的语言严格证明，初学时这两个结论会用即可。

扎实的概率论功底对将来的科研起到决定性的作用。从我自身的经历来看，我觉得大一大二最有用的专业课就是数分、高代和概率论，后续一切课程本质上都是这三门课的应用。

**数理统计**

官方教材：

1. 陈家鼎, 孙山泽, 李东风, and 刘力平. *数理统计学讲义*. 高等教育出版社, 2015.
2. George Casella, and Roger L. Berger. *Statistical inference*. Cengage Learning, 2021.
3. Jun Shao. *Mathematical statistics*. Springer Science & Business Media, 2003.

前两本为普通版教材，第三本为数理统计实验班以及高等统计学的教材。[第一本非常不推荐](https://www.zhihu.com/question/438130809/answer/1664210460)，此书写作风格过于晦涩，初学者不易读懂，且内容较为陈旧。第二本是初等数理统计非常好的入门教材，第三本适合熟悉测度论的人，但实验班授课时不讲授涉及测度论的证明。其他推荐课本和阅读材料可见[李通宇学长的个人主页](http://scholar.pku.edu.cn/lity/classes/21F-MathStatH-TA/materials/readings)。这里个人认为比较好的自学教材是：

Wasserman, Larry. *All of statistics: a concise course in statistical inference*. Vol. 26. New York: Springer, 2004.

## 分析功底：实变函数、测度论、泛函分析、偏微分方程

**实变函数**

官方教材：

1. 周民强. *实变函数论*. 北京大学出版社, 2016. 

2. Elias M. Stein, and Rami Shakarchi. *Real analysis: measure theory, integration, and Hilbert spaces*. Princeton University Press, 2009.

其他推荐教材：Gerald B. Folland. *Real analysis: modern techniques and their applications*. Vol. 40. John Wiley & Sons, 1999.

周民强课本可谓是实变函数理论的集大成者，内容非常充实，但这也造成初学时难以把握重点，且习题难度较大。初学建议用Stein（前三章），此书理论体系非常清晰，行文流畅且证明直观，自学起来不太累。可以等Stein学完以后再看周民强，或者把周民强当做考前习题集。

**测度论**

官方教材：程士宏. *测度论与概率论基础*. 北京大学出版社, 2006.

这本书写得还不错，理论体系也非常清晰，除去排版不够美观以外没什么不足之处。课程会讲授前四或五章，最后一章会放在高等概率论中讲授。

测度论和实变两门课重合程度比较高。实变主要研究的是$\mathbb{R}^d$上的Lebesgue测度，包含点集拓扑、Lebesgue测度的建立、Lebesgue积分、求导与积分间的关系（Newton-Leibnitz公式）和$L^p$空间等内容，而测度论研究的是更为一般的测度空间$(X,\mathcal{F},\mu)$，研究其上集合系的关系、半环上测度扩张到$\sigma$域上、积分、$L^p$空间、求导与积分间的关系（Radon-Nikodym导数）以及（有穷维、可列维、任意无穷维）的乘积空间。因此，学过一门以后学另一门相对容易，大部分学生是先学实变后学测度论，如果想抄捷径的话可以直接看Folland书的前三章，这里涵盖了实变和测度论课程中的大部分内容。

**泛函分析**

官方教材：张恭庆, and 林源渠. *泛函分析讲义（上册）*. 北京大学出版社, 2021.

其他推荐教材：Theo Bühler, and Dietmar Salamon. [*Functional analysis*](people.math.ethz.ch/~salamon/PREPRINTS/funcana-ams.pdf). American Mathematical Society, 2018.

==暂无评价==

**偏微分方程**

官方教材：周蜀林. *偏微分方程*. 北京大学出版社, 2008.

其他推荐教材：Lawrence C. Evans. *Partial differential equations*. Vol. 19. American mathematical society, 2022.

本质上周蜀林书是Evans书一小部分的中文翻译版。Evans书可以算是PDE领域的百科全书，行文流畅，可直接照此学习。

==暂无评价==

## 概率统计进阶：高等概率论、随机过程（包括随机微分方程）、高维概率论与高维统计学

**高等概率论**

官方教材：Rick Durrett. [*Probability: theory and examples*](https://services.math.duke.edu/~rtd/PTE/PTE5_011119.pdf). Vol. 49. Cambridge university press, 2019.

==暂无评价==

**随机过程（包括随机微分方程）**

章复熹老师应用随机过程（实验班）课程主页（[讲义](https://www.math.pku.edu.cn/teachers/zhangfxi/homepage/textbook.htm)，[课件](https://www.math.pku.edu.cn/teachers/zhangfxi/homepage/slidesSPA.htm)）.

[刘勇老师应用随机分析课程主页（含讲义）](https://www.math.pku.edu.cn/teachers/liuyong/teachingindex.html).

E Weinan, Tiejun Li, and Eric Vanden-Eijnden. *Applied stochastic analysis*. Vol. 199. American Mathematical Soc., 2021.

Bernt Øksendal. [*Stochastic differential equations: an introduction with applications*](https://link.springer.com/book/10.1007/978-3-642-14394-6). Springer Science & Business Media, 2013.

==暂无评价==

**高维概率论与高维统计学**

官方教材：Roman Vershynin. [*High-dimensional probability: An introduction with applications in data science*](https://www.math.uci.edu/~rvershyn/papers/HDP-book/HDP-book.pdf). Vol. 47. Cambridge university press, 2018.

其他推荐教材：

1. Ramon van Handel. [*Probability in high dimension*](https://web.math.princeton.edu/~rvan/APC550.pdf). PRINCETON UNIV NJ, 2014.

2. Martin J. Wainwright. *High-dimensional statistics: A non-asymptotic viewpoint*. Vol. 48. Cambridge University Press, 2019.

==暂无评价==


## 计算相关：数值代数、数值分析、偏微分方程数值解

==暂无评价==

## Python编程

### 入门

这部分包括Python基本操作以及一些基础的数据结构和算法知识，大一的“计算概论”和“数据结构与算法”会覆盖。

编程语言为什么推荐Python，因为：1. Python是目前最热门的编程语言之一，且在机器学习和深度学习中具有压倒性地位；2. Python为开源语言，社区生态经过多年发展非常完善，相比之下MATLAB为专注科学计算的[商业软件](https://zhuanlan.zhihu.com/p/147901519)；3. Python的难度远小于C/C++。

如果想修信科的双学位（俗称“软双”）则需大一上修信科的“计算概论A”，这门课应该讲C++，Python完全可以自学。

### 进阶

这部分包括统计学习和深度学习的一些软件包的使用。

前者最重要的`numpy`（用于矩阵运算）和`matplotlib`（用于绘图）这两个包，也包括`scipy`（常用的科学计算）、`sklearn`（统计学习）、`pandas`（处理表格数据，类似 `Excel` ）等。

后者可在`torch`、`tensorflow`和`jax`中任选一种。目前学界最常用的应该是`torch`，且发展迅猛；业界`tensorflow`也比较常用，但总体来看发展在放缓；`jax`的生态还处于建设阶段，过几年会比较成熟。

推荐书籍：Eli Stevens, Luca Antiga, and Thomas Viehmann. *Deep learning with PyTorch*. Manning Publications, 2020.

这本书比较详尽地介绍了`torch`的主要功能，且[作者在GitHub上提供了所有教学代码](https://github.com/deep-learning-with-pytorch)，非常适合自学。

## 优化

Stephen P. Boyd, and Lieven Vandenberghe. [*Convex optimization*](https://web.stanford.edu/~boyd/cvxbook/). Cambridge university press, 2004.

## 统计学习

Hastie, Trevor, et al. [*The elements of statistical learning: data mining, inference, and prediction*](https://link.springer.com/book/10.1007/978-0-387-84858-7). Vol. 2. New York: springer, 2009.

Andrew Gelman, John Carlin, Hal Stern, David Dunson, Aki Vehtari, and Donald Rubin. [*Bayesian data analysis*](http://www.stat.columbia.edu/~gelman/book/). Chapman and Hall/CRC, 2015.

Bishop, Christopher M., and Nasser M. Nasrabadi. *Pattern recognition and machine learning*. Vol. 4. No. 4. New York: springer, 2006.

## 深度学习

Ian Goodfellow, Yoshua Bengio, and Aaron Courville. [*Deep learning*](https://www.deeplearningbook.org/). MIT press, 2016.

## 理论机器学习

1. Mehryar Mohri, Afshin Rostamizadeh, and Ameet Talwalkar. [*Foundations of machine learning*](https://www.dropbox.com/s/38p0j6ds5q9c8oe/10290.pdf?dl=1). MIT press, 2018.
2. Francis Bach. [*Learning Theory from First Principles*](https://www.di.ens.fr/~fbach/ltfp_book.pdf). 
3. Shai Shalev-Shwartz, and Shai Ben-David. [*Understanding machine learning: From theory to algorithms*](https://www.cs.huji.ac.il/w~shais/UnderstandingMachineLearning/understanding-machine-learning-theory-algorithms.pdf). Cambridge university press, 2014.
4. Matus Telgarsky. *Deep learning theory lecture notes* ([HTML version](https://mjt.cs.illinois.edu/dlt/), [PDF version](https://mjt.cs.illinois.edu/dlt/index.pdf)).

## 强化学习

Richard S. Sutton, and Andrew G. Barto. [*Reinforcement learning: An introduction*](http://incompleteideas.net/book/the-book-2nd.html). MIT press, 2018.

*未完待续*



| **<a href="/index.html">返回主页</a>** | **最后更新：2022年7月14日** |
