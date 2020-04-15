# Sklearn-Algorithm
## 线性回归
**简单线性回归(simple linear regression)** 简单线性回归通常就是包含一个自变量x和一个因变量y，这两个变量可以用一条直线来模拟。如果包含两个以上的自变量就叫做**多元回归(multiple regresseion)** 被用来描述因变量y和自变量x以及偏差error之间关系的方程叫做回归模型<br>
### 损失函数
!()[] <br>
对于这个损失函数，一般有梯度下降法和最小二乘法两种极小化损失函数的优化方法，sklearn中提供的LinearRegression用的是最小二乘法，因为最小二乘法在概率论，统计学等课中学过，所以在这里详细讲解梯度下降法。<br>
**[梯度下降算法](https://www.jianshu.com/p/386645b7e03a)** 梯度下降法是一种在学习算法及统计学常用的最优化算法，其思路是对theta取一随机初始值，可以是全零的向量，然后不断迭代改变θ的值使其代价函数J（θ）根据梯度下降的方向减小，直到收敛求出某θ值使得J（θ）最小或者局部最小。其更新规则为：

- 为什么梯度下降可以逐步减小代价函数
 - 假设函数`f(x)`
 - 泰勒展开：`f(x+△x)=f(x)+f'(x)*△x+o(△x)`
 - 令：`△x=-α*f'(x)`   ,即负梯度方向乘以一个很小的步长`α`
 - 将`△x`代入泰勒展开式中：`f(x+△x)=f(x)-α*[f'(x)]²+o(△x)`
 - 可以看出，`α`是取得很小的正数，`[f'(x)]²`也是正数，所以可以得出：`f(x+△x)<=f(x)`
 - 所以沿着**负梯度**放下，函数在减小，多维情况一样。




**线性回归的目的是要得到输出向量Y和输入特征X之间的线性关系，求出`线性回归系数`。为了得到线性回归系数θ，我们需要定义一个`损失函数`，一个极小化损失函数的优化方法，以及一个验证算法的方法。损失函数的不同，损失函数的优化方法的不同，验证方法的不同，就形成了不同的线性回归算法。**


Sklearn机器学习中的主要算法原理以及实现
