# RUC_MachineLearning2020
Machine Learning courses in RUC, School of Statistics

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
## HW5
## HW6
## HW7
## HW8
