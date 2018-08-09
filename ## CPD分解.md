# *Tensor Decompositon*
## 张量分解
### 张量介绍
#### 张量的秩
1. 最大秩：极大秩是定义为可获得的最大秩
2. 特定秩：特定秩是任何存在于大于零且张量部分满足一致连续分布。
*typical rank is
any rank that occurs with probability greater than zero (i.e., on a set with positive
Lebesgue measure)*
#### 奇异值分解（SVD）
1. 概念：形如[![201101192226335092.png](https://s19.postimg.cc/5w98n4pxv/201101192226335092.png)](https://postimg.cc/image/nz2beclsf/)这样的，A是一个N\*M的矩阵。U是N\*N方针，称为左奇异向量。Σ是一个N\*M矩阵（除了对角线，其余元素都为0，对角线上的元素被称为奇异值）V'是M\*M方阵，同U，称为右奇异向量。
#### 主成分分析（PCA）
* PCA是最重要的降维方法之一，在数据压缩消除冗余和数据噪音消除等领域都有广泛的应用。
* 降维标准：样本点到这个超平面的距离足够近，或者说样本点在这个超平面的投影尽可能分开
* PCA推导：基于小于投影距离 
[![image.png](https://s19.postimg.cc/sv1tbqinn/image.png)](https://postimg.cc/image/kpjrdkuen/)
	
### 应用
1. 在广泛的信号过程和数据分析分支中，CPD已经地成为作为信号分离的高级工具
2. 在是这一次我知道的认识
	* 难点
		* 张量的秩的定义是模仿矩阵秩定义的方法，但是矩阵和张量的秩的特性十分不同。首先，一个实值张量可能远远不同于R和C的实数域
		* 张量和矩阵秩最大的不同是，这里没有直接的算法来确定的一个特定的张量。
		* 另外不同的是，张量必须知道其最大和特定秩。
	* 幸运的是，在信号过程的应用中，秩的估计可以确定被找到符合充分精确的张量元素
3. 符号
	* mode-n product: 张量A属于R(I1XI2...IN)，B属于R(JnXIn)，乘积出的C属于R(I1X...XIn-1XJnXIn+1X...XIN)
$$x = {-b \pm \sqrt{b^2-4ac} \over 2a}.$$
$\sqrt{3x-1}+(1+x)^2$
	
### 计算
1. 由于CPD的计算在本质上是多线性的，我们可以通过交替最小二乘结构得到一系列线性子问题的结果，同时在保持其他要素满足条件的情况下，通过最小二乘法依次选择合适高效的要素矩阵。根据Khatri–Raoproducts，
### EXAMPLE
	* example1
	* 考虑一个张量向量它包含K和恒等子列阵I张量，I`=KI总共
	* 对于R窄带
### TKD和CPD区别
1. 符号标记（CPD和TKD的区别）
	* CPD采用的是点乘（KHATRI-RAO乘积），即IxR和JxR。
	* TKD采用的是叉乘（KRONECKER乘积），即I1xI2和J1xJ2。
	* 结果C=AxB规模都为I1I2xJ1J2
	
### 张量矩阵化（matricization）
* 意义:转化一个张量为矩阵，也称为unfloding或者flattening，是重组N维向量为一个矩阵，例如，一个2x3x4张量可以重组维6x4的矩阵或3x8的矩阵等。我们考虑mode-n矩阵化因为这是和我们讨论相关的形式。n-mode张量矩阵化X属于R(I1XI2..XIN)可以标记为X（n）
* 		 
---
	
### 英文翻译
#### 单词短语

|单词|翻译|
| :- | -: |
|real-valued| adj.实值的|
|determine  |verb.确定|
|typical |典型；特定的|
|uniform continous distribution| 一致连续分布|
|correspond to |符合|
|pragmatic |adj.实用的|
|irration |n.无理数|
|factor |n.因子|
|explicit |adj.明确的|
|intrinsical |adj.本质的|
|whereby |adv.通过...;借以；|
|algorithm |n.算法|
|subarray |n.子列阵|
|narrowband| n.窄带|
|snapshot |n.快照|
|Matricization/folding |n.展开|
|versa |n.反的|
|proposition |n.命题|
|orthonormal |adj.标准正交的
|truncated|adj.缩短的，被删节的|
|optimal、optimization、optimize|adj.最优的，n.最优化，vt.使最优化，使...最有效|
|iterative|adj.迭代的|
|eigenvalue|n.特征值|
|cease|v.停止|
|quadratic|adj.二次的|
|propertie|n.特性|
|sparse|adj.稀疏的|

#### 专业词组以及缩写
|英文全称（缩写）|翻译|
| :-: | :-: |
|alternating least square(ALS)| 交替最小二乘法|
|least squares（LS）|最小二乘法|
|signal-to-noise ratio(SNR) |信躁比|
|cost function |成本函数|
|component matrix| 因子矩阵；初始因子载荷阵|
|principal component analysis （PCA）|主成分分析|
|independent component correlation algorithm（ICA）| 独立成分分析|
|the canonical polyadic decomposition(CPD）|正则多项式分解|
|The Tucker decomposition （TKD）|tucker分解|
|block term decomposition (BTD) |块项分解|
|the matrix singular value decomposition（SVD）|矩阵奇异值分解|
|CANDECOMP/PARAFAC decomposition |CP分解|
|blind source separation （BSS）|盲信号分离|
|location-based social networds(LBSNS)||
### 图片记录
---
[![image.png](https://s19.postimg.cc/t2t4j1as3/image.png )](https://postimg.cc/image/j5i3pz367/)      
*三维张量在CPD和TUCKER下的不同表现形式*    
---
[![image.png](https://s19.postimg.cc/kafu6lh83/image.png)](https://postimg.cc/image/rdnpm7mnj/)  
*不同乘积的定义*  
---
[![image.png](https://s19.postimg.cc/ad4tdkzcj/image.png)](https://postimg.cc/image/8y38ouy9b/)  
*TUCKER分解*  
---
[![1531893071_1.png](https://s19.postimg.cc/6e3xjptgz/1531893071_1.png)](https://postimg.cc/image/go6ciyjcf/)  
*the higher-order orthogonal iteration算法*
### MATLAB 代码
	* Y = randn(m,n,p,...) ：产生随机数组
	* 
