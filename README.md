# RUC_MachineLearning2020
Machine Learning courses in RUC, School of Statistics

notes(笔记内容): https://www.jianshu.com/nb/44642000

## HW1
### 口罩真伪概念学习任务
已知：

* 实例集X：口罩数据，每个口罩数据由以下属性描述：
	1. 口罩下方的数字序列是否清晰：（可取值 “是”和“否”）
	2. 字体是否是斜纹45度喷墨上去的：（可取值 “是”和“否”）
	3. 金属条是否光滑：（可取值 “是”和“否”）
	4. 是否有异味：（可取值 “是”和“否”）
	5. 口罩上的中英文是否清晰：（可取值 “是”和“否”）
	6. 是否有QS认证或LA认证：（可取值 “是”和“否”）
	7. 是否有呼吸阀：（可取值 “是”和“否”）
* 假设集H：每个假设描述为7个属性值的约束合取，其中“？”表示接受任意值，“ø” 表示拒绝所有值或一特定值
* 目标概念C：口罩真伪：X -> {0,1}
* 训练样例集D：目标函数的正例和反例

求解：
* H中的一假设h， 使对于X中任意x , h(x) = c(x) 
## HW2
### Auto数据集
(a)将数据集按照留出法划分为训练集和测试集(比例为80%和20%)，对于函数mpg = 40 - 0.15 * horsepower 编写程序估计平方损失下的泛化误差，自行设定实验次数进行泛化

(b)将数据集按照留p交叉验证的方式提取测试集， K=20划分采取无放回抽样p = 10， 对于函数mpg = 40 - 0.15 * horsepower 编写程序估计平方损失下的泛化误差

(c)建立一个二元变量，每加仑里程量(mpg01)，1表示每加仑汽油该型号车所跑里程数(mpg)在3/4分位数一下。将数据集按照留出法随机分为训练集和测试集(比例为80%和20%)，对于函数P(mpg01 = 1) = exp{3.85 - 0.01 * weight}/(1 + exp{3.85 - 0.01 * weight})
编写程序估计平方损失下的泛化误差

(d)将数据集按照分层等比例划分为训练集和测试集(比例为80%和20%)，对函数P(mpg01 = 1) = exp{3.85 - 0.01 * weight}/(1 + exp{3.85 - 0.01 * weight})编写程序估计平方损失下的泛化误差

(e)根据以上实验结合教材，分析不同划分和抽样方式对泛化误差的影响
## HW3
### 钓鱼数据集和手写体数据集
1. 在一个钓鱼问题(fishing.xls)，感兴趣的是具备怎样的条件可以钓到鱼，数据被划分为训练集和测试集(根据标签变量)，在训练集上建立了两个模型，分别获得了测试和训练集的预测评分E(Y|X)的估计，要求编写程序，实现一下分析内容，做出数据分析报告

* 对训练数据和测试数据分别对模型1和模型2制作P-R图，ROC曲线，估计AUC面积，判断整体预测效果。如果按照实验结果给出一个符合实际的阈值，请说明阈值的选取依据

* 在给出阈值上输出混淆矩阵

* 如果将钓不到鱼的游客判为能钓到鱼，这个损失会使钓鱼中心声誉受到更大损失，将该损失设为能钓到鱼的游客判为钓不到鱼的损失的2倍，根据新的非平衡代价损失制作两个模型的测试数据的代价曲线，给出比较分析结果。

2. 在一个汉字识别问题中(handwriting.xls)，用5折交叉验证将书籍分成5折训练集和测试集，获得了三个0-1分类模型

* 编写程序计算宏、微查全率和查准率，根据经验选择合适的阈值

* 编写程序求解期望代价曲线， 并画图表示

* 给出5折交叉验证的binominal检验误差的检验结果，分析这两种结果的差异

* 根据Friedman检验判断分类器性能差异是否显著

## HW4
### Boston数据集与Credit数据集
1. 请用Boston数据中的medv对lstat建模，线性模型，二次模型和knn模型，在使用knn回归的时候可以尝试不同的k，比较拟合效果，输出结果，分析结果。

2. 使用Credit数据建立回归,用balance对rating,limit和age建立回归模型：

* 编写程序用least square算法分别计算balance对每个自变量的一元回归系数；

* 用least square计算balance对limit和rating的回归，请比较2和1的回归系数之间的差异；

* 用least square计算balance对age和rating的回归，请比较3和1的回归系数之间的差异；

* 请用正交系数估计算法计算balance对age和rating的回归，请分析1,2,3,4回归系数的不同
## HW5
### 心脏病数据集

* 在sa心脏数据中，用chd(1:得病，0:正常)对tobacco+ldl+age进行logistics回归建模，预测一个人得心脏病的概率，使用梯度下降算法来得到迭代估计，返回系数估计

* 用心脏病数据进行LDA建模，计算w，估计健康人和得病人的三个输入变量的协方差矩阵和每个类的均值位置，再根据训练数据判错率最低的要求选择w0，返回系数估计，并且和w = (0.61, -0.45, 0.65)所给出的判别面的效果进行比较

## HW6
### Boston数据集和smarket数据集
1.1 个人作业：对于课件4.8-4.10中有关有样本协方差矩阵不等的情况，QDA的例题，采用模拟数据，使用两种等协方差矩阵LDA和Fisher判别的结果如何，请输出训练误差并作图来回答这个问题。

1.2.个人作业：对于Boston房价数据，用最后一列房价，按照1/4分位数，中位数和3/4分位数将其分成四段，请使用industry,river,nox,rooms，age,distance几个自变量进行OvO设计和MvM设计，编写程序对LDA进行多分类分析。

2.1.小组大作业，对于SP&500案例数据smarket，我们在课堂上一共提供了四种方法的比较，在这个股票价格涨跌的分析中，你们认为对涨跌预测比较可行的分析步骤有哪些（包括训练集与测试集的不同划分方式（比较留出法和交叉验证），引入模型的变量数（2个还是7个），不同的模型（Logistic,LDA,QDA还是Fisher判别（降维还是原矩阵） ），请组内讨论，选择其中至少两个步骤开展实验，写成数据分析报告（R Markdown 或Jupyter notebook）。

## HW7
### 西瓜数据集
* 试编程实现基于信息熵进行划分选择的决策树算法，并为数据集生成一棵决策树

## HW8
### 西瓜数据集3.0
* 试编程实现一种多变量决策树算法

## HW9
### 西瓜数据集3.0alpha
* 试编程实现AdaBoost，以不剪枝决策树为基学习器，在西瓜数据集上生成一个AdaBoost集成

## HW10
### 西瓜数据集3.0
* 试编程实现标准BP算法和累积BP算法，在西瓜数据集3.0上分别用着两个算法训练一个单隐层网络，并进行比较
### UCI数据库中的fgl数据
* 将fgl数据集中的6种玻璃类型作为输出变量，用神经网络构建单隐层模型，使用sigmoid激活函数，选择损失函数，根据梯度下降法，把训练误差当作泛化误差，比较不同的节点数量(2,3,4,5)之间的训练误差有怎样的不同
* 用scikit-learn中的逻辑回归模型建立回归，导出训练误差率，比较1和2之间的差异

## HW11
* 请学习如下程序，并对实验训练数据进行RBF分类，用测试数据定义误差函数，预设学习率，调节权值以及中间层神经元个数M，输出对不同的隐层数和不同的sigma对测试误差的影响，从中能够对M的大小和sigma的大小和对测试误差的影响有怎样的认识？
参考github：shiliuqiang/RBF_NN_Python

* 学习github项目Solving the Traveling Salesman Problem using Self-Organizing Maps，调整学习率、更新半径以及结点数量，观察结果变化

* 5.8.3选做：Python机器学习P218页，下载MNIST数集，实现一个多层感知机模型，尝试将激活函数更新为RBF，比较Sigmoid激活函数和RBF的效果
