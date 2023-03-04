
a Excel training

#主题:(电商类型数据分析)研究婴儿产品与婴儿年龄与商品间关系


#数据源:该数据集来自阿里天池


#原始数据如下图所示
1.用户id宝宝的性别以及生日时间(未经任何处理)


![image](https://github.com/Lzt438/Excel/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202023-03-04%20112713.png)


2.用户id的购买商品数量、购买时间、商品类别、商品种类ID等(未经任何处理)


![image](https://github.com/Lzt438/Excel/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202023-03-04%20112752.png)


数据清洗：

1.将表格中的英文字段改为中文字段

2.隐藏无意义的字段

3.将用户ID改为数字格式，并对其升序排列

4.查找并删除重复用户ID，查找并删除缺失值

5.将购买时间与出生日期改为日期格式,将性别字段改为0--男, 1--女, 2--未知

清洗后的数据如下图：

![image](https://github.com/Lzt438/Excel/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202023-03-04%20115408.png)


![image](https://github.com/Lzt438/Excel/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202023-03-04%20115409.png)

根据购买数量排序后,发现有一个用户的购买数量为1000,严重大于其他值,去除掉此异常值
去除后，按用户ID合并两表

通过购买时间与宝宝出生时间,算出宝宝年龄得到如下数据

![image](https://github.com/Lzt438/Excel/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202023-03-04%20152109.png)
