
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

通过购买时间与宝宝出生时间,算出宝宝年龄,观察数据,发现其中有一个数据的宝宝年龄显示位28岁,远大于其他值,故删去,同时还存在少数用户购买时间的缺失,故删去
得到的数据如下图:


![image](https://github.com/Lzt438/Excel/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202023-03-04%20152109.png)


根据合并后的数据表插入的数据透视表如下:

1.商品类别与购买数量

![image](https://github.com/Lzt438/Excel/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202023-03-04%20181511.png)


![image](https://github.com/Lzt438/Excel/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202023-03-11%20162555.png)


可知"50008618"和"50014815"这两类商品购买数量较多

2.宝宝性别与婴儿商品购买数量间的关系

![image](https://github.com/Lzt438/Excel/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202023-03-04%20182349.png)

使用Tableau做出的条形图如下图所示:


![image](https://github.com/Lzt438/Excel/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202023-03-11%20163038.png)


可知男宝宝的婴儿商品购买数量多于女宝宝


3.宝宝年龄以及商品类别与商品购买数量的关系

![image](https://github.com/Lzt438/Excel/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202023-03-03%20172245.png)


使用Tableau作出的堆积图如下图所示:


![image](https://github.com/Lzt438/Excel/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202023-03-12%20162244.png)



可知宝宝年龄为0-1岁的用户购买商品类别为"50014815"的商品数量最多,宝宝年龄为2-8岁的用户购买商品类别为"50008168"的商品数量最多,购买人群主要集中在宝宝年龄为0-5岁之间的用户
