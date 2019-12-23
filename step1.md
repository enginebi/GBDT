## 理解GBDT算法

看这篇文章: https://www.ctolib.com/topics-142338.html
再结合https://github.com/Freemanzxp/GBDT_Simple_Tutorial  基本可以理解gdbt的算法流程。

## 重要度计算

[en](https://www.cnblogs.com/wuxiangli/p/6756577.html)
[cn](https://www.zybuluo.com/yxd/note/614495)

## 数据集

### 导入数据集

```
import pandas as pd
from sklearn import datasets

iris_data=pd.read_csv('boston_house_prices.csv')
# iris_data.columns=['CRIM','ZN']
print(iris_data)
print(iris_data.columns)
print(iris_data.head(5))# iris_data.head(5) #可以查看一下前5行数据，检查是否读取正确
# iris_data['class'] = iris_data['class'].apply(lambda x: x.split('-')[1]) #最后类别一列，感觉前面的'Iris-'有点多余即把class这一列的数据按'-'进行切分取切分后的第二个数据，为了好看一点点
# print(iris_data.describe())#使用describe()可以很方便的查看数据的大致信息，可以看到数据是没有缺失值的，总共有145条，每一列的最大值、最小值、平均值、分位数都可以查看。

boston = datasets.load_boston()
print(boston)
print(boston['feature_names'])
```