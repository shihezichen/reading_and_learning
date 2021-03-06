# 1.引言
-------2020-2-11--------------------  
## 本书面向的读者
## 深度学习的历史趋势
分布式表示  
### 神经网络的众多名称和命运变迁
### 与日俱增的数据量
### 与日俱增的模型规模
### 与日俱增的精度，复杂度和现实世界的冲击
# 2.线性代数
## 标量、向量、矩阵和张量
广播
## 矩阵和向量相乘
## 单位矩阵和逆矩阵
## 线性相关和生成子空间
## 范数
L2范数  
平方L2范数  
L1范数---区分0和非零的时候使用该范数  
L0范数---向量中非零元素的个数但该范数数学不严谨，常使用L1范数代替  
最大范数---向量元素中绝对值最大值  
Frobenius范数---矩阵所有元素的平方和的平方根  
## 特殊类型的矩阵和向量
对角矩阵，对称矩阵，正交矩阵
## 特征分解
矩阵跟特征向量相乘相当于将特征向量进行方法特征值倍  
实对称矩阵一定可以特征值分解，将特征值按照降序排列可以获得唯一的分解结果  
矩阵的特征分解可以用来优化二次方程  
## 奇异值分解
每个实矩阵都存在奇异值分解  
## Moore-Perose伪逆
## 迹运算
## 行列式
## 实例：主成分分析

# 3.概率与信息论
## 为什么要是用概率
被建模系统内在随机性  
不完全观测  
不完全建模  
## 随机变量

## 概率分布
### 离散型变量和概率质量函数
### 连续型变量和概率密度函数 

## 边缘概率
## 条件概率
## 条件概率的链式法则
## 独立性和条件独立性
## 期望、方差和协方差
## 常用概率分布
### Bernoulli分布  
### Multinoulli---常用来表示对象分类的分布  
-----------2020-2-11---------------  
### 高斯分布
中心极限定理说明多个独立随机变量的和近似服从正态分布  
在相同方差的所有实数分布中正态分布具有最大的不确定性---正态分布是对模型加入先验知识最少的分布
### 指数分布和Laplace分布
### Dirac分布和经验分布
经验分布可以被定义成一个多项式分布，对每一个可能的输入，其概率可以简单地设为训练集那个输入的经验概率  
关于经验分布另外一个观点是它是训练集上似然最大的那个概率分布  
### 分布的混合
数据集经验分布被表示成dirac为基本组件的混合分布  
潜变量---不能直接观测到的随机变量  
高斯混合模型---万能近似器  
### 常用函数的有用的性质
logistic sigmoid函数  
softplus函数  

正部函数x+=max(0,x) 
负部函数x-=max(0,-x)  
### 贝叶斯规则
### 连续型变量的技术细节
### 信息论
对一个信号包含多少信息进行量化  
自信息  
香浓熵  
KL散度---描述两个分布之间的差异，具有不对称性  
离散KL散度的物理意义：当我们使用一种被设计成使得概率分布Q产生的消息的程度最小的编码，发送由概率分布P产生的符号信息时，所需要的额外信息量  
交叉熵  
信息论中0log0==0  
## 结构化概率模型
概率 图 
有向、无向  
# 4.数值计算
## 上溢、下溢
softmax()函数  
下溢---接近0的数字被四舍五入到0  
上溢---数字太大被当做无穷  
## 病态条件
## 基于梯度的优化方法
梯度之上：Jacobian和Hessian矩阵
数值优化  
## 约束优化
在某些集合中寻找最大值和最小值  
设计一个无约束优化问题，求出来的解再转化为约束优化问题的解  
KKT方法  
## 实例：线性最小二乘

# 5.机器学习基础
## 学习算法
### 任务T
分类、输入缺失分类、回归、转录、机器翻译、结构化输出、异常检测、合成和采样、缺失值填补、去噪、密度估计或者概率质量函数估计  
### 性能度量P
取决于应用场景  
### 经验E
### 线性回归

## 容量，过拟合和欠拟合
泛化  
过拟合、欠拟合  
### 没有免费午餐定理
### 正则化
通过控制函数种类和函数数量来控制算法性能  
## 超参数和验证集  
------2020-2-12-----------------  
验证集---筛选超参数  
K-折交叉验证  
## 估计、偏差和方差
### 点估计
### 偏差
无偏、渐进无偏  
### 方差和标准差
### 权衡方差和偏差以最小化均方误差
增加容量会增加方差，降低偏差  
### 一致性
渐进无偏跟一致性不是一回事  
## 最大似然估计
### 条件对数似然和均方误差
最大化似然得到的参数跟最小化均方误差得到的参数相同，但是两个目标函数的值是不同的  
### 最大似然的性质
有参估计中，当样本数量足够大，不存在均方误差低于最大似然估计的一致估计---克拉美罗下界  
当样本数量有限的时候，会发生过拟合，使用正则化可以降低训练的方差，或者最大似然的有片版本  
## 贝叶斯统计
当训练数据较少的时候，贝叶斯推断可以表现非常好的特性，但是当数据量很大，贝叶斯推断的计算量非常巨大  
### 最大后验估计


## 监督学习算法
### 概率监督学习
### 支持向量机
### 其他简单的监督学习算法
## 无监督学习算法
### 主成分分析
也可以使用SVD分级，设计矩阵X的有奇异矩阵作为对X的线性变换，得到的新的矩阵，在方差上，各个变量之间切断了联系，进一步降维  
### K均值聚类
### 随机梯度下降
优化的量不会随着样本数量的增加而增加，会保持一定的规模，降低计算时间  
---------2020-2-13-----------  
## 构建机器学习算法
## 促使深度学习发展的挑战
### 维数灾难  
随着维数的增加，模型的维度指数增加  
### 局部不变性和平滑正则化
为了更好的泛化，需要由先验信念引导应该学习什么类型的函数  
平滑先验---我们学习的函数在小区域内不会发生很大的变化---对于复杂的人工智能问题效果不好  
可以通过k个样本点产生指数个区分区间  
### 流形学习

# 6.深度前馈网络
深度前馈网络---前馈神经网络---多层感知机  
深度前馈网络定义了一个映射，通过学习参数，找到最佳的函数近似  

## 实例：学习XOR
线性函数不能学习异或，加入激活函数，处理非线性  
## 基于梯度的学习
----------2020-2-14--------------  
将权重初始化为小的随机数，将偏置初始化为0或者正的小随机数  
### 代价函数  
大多数神经网络使用最大似然来训练  
均方误差和绝对值误差的梯度优化效果不佳，更广泛的是使用交叉熵代价函数  
### 输出单元
用于高斯输出分布的线性单元  
用于Bernoulli输出分布的sigmoid单元  
用于Multinoulli输出分布的softmax单元  
























