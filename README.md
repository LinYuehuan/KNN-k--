[K近邻算法](http://www.cnblogs.com/ybjourney/p/4702562.html)
====
# 一 . K-近邻算法（`KNN`）概述<br>
&emsp;&emsp;最简单最初级的分类器是将全部的训练数据所对应的类别都记录下来，当测试对象的属性和某个训练对象的属性完全匹配时，便可以对其进行分类。但是怎么可能所有测试对象都会找到与之完全匹配的训练对象呢，其次就是存在一个测试对象同时与多个训练对象匹配，导致一个训练对象被分到了多个类的问题，基于这些问题呢，就产生了KNN。<br>

&emsp;&emsp;KNN是通过测量不同特征值之间的距离进行分类。它的的思路是：如果一个样本在特征空间中的k个最相似(即特征空间中最邻近)的样本中的大多数属于某一个类别，则该样本也属于这个类别。K通常是不大于20的整数。KNN算法中，所选择的邻居都是已经正确分类的对象。该方法在定类决策上只依据最邻近的一个或者几个样本的类别来决定待分样本所属的类别。<br>

&emsp;&emsp;下面通过一个简单的例子说明一下：如下图，绿色圆要被决定赋予哪个类，是红色三角形还是蓝色四方形？如果K=3，由于红色三角形所占比例为2/3，绿色圆将被赋予红色三角形那个类，如果K=5，由于蓝色四方形比例为3/5，因此绿色圆被赋予蓝色四方形类。<br>

![](http://images0.cnblogs.com/blog2015/771535/201508/041623504236939.jpg)<br>

&emsp;&emsp;由此也说明了KNN算法的结果很大程度取决于K的选择。<br>

&emsp;&emsp;在KNN中，通过计算对象间距离来作为各个对象之间的非相似性指标，避免了对象之间的匹配问题，在这里距离一般使用欧氏距离或曼哈顿距离：<br>

&emsp;&emsp;同时，KNN通过依据k个对象中占优的类别进行决策，而不是单一的对象类别决策。这两点就是KNN算法的优势。<br>

&emsp;&emsp;接下来对KNN算法的思想总结一下：就是在训练集中数据和标签已知的情况下，输入测试数据，将测试数据的特征与训练集中对应的特征进行相互比较，找到训练集中与之最为相似的前K个数据，则该测试数据对应的类别就是K个数据中出现次数最多的那个分类，其算法的描述为：<br>

+	计算测试数据与各个训练数据之间的距离；<br>

+	按照距离的递增关系进行排序；<br>

+	选取距离最小的K个点；<br>

+	确定前K个点所在类别的出现频率；<br>

+	返回前K个点中出现频率最高的类别作为测试数据的预测分类。<br>

&emsp;&emsp;next is code:

	#include <stdio.h>

	int main(void){
		return 0;
	}
&emsp;&emsp;next is img:

![This is a test img!](https://github.com/LinYuehuan/KNN/blob/master/img/1.jpg "test img")