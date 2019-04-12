---
layout: page
mathjax: true
permalink: /2018/projects/p08/midterm/
---

## 项目进展报告

### 数据获取及预处理

数据来自天池大数据竞赛的初赛阶段，包括训练文件d\_train.csv和测试文件d\_test.csv，其中训练文件共包含5642条记录，每条记录42个字段，包含数值型、字符型、日期型等众多数据类型，部分字段内容在部分人群中有缺失，其中第一列为个体ID号。训练文件的最后一列为标签列，既需要预测的目标血糖值。因为数据存在缺失值、以及各个数据的尺度不一，需要进行填补缺失值和归一化等处理。

### 数据分析与可视化

对数据集做初步的探索性分析，得到训练数据集和测试数据的基本统计描述，有效记录数、各个数值字段的最大值、最小值、均值、标准差见表 _初步统计情况.xlsx_ 。

### 模型选取

首先选择了最简单的logistic回归模型分析与糖尿病（即血糖值偏高）相关的危险因素，并对血糖值进行预测以及给出变量重要性排序。

### 挖掘实验的结果

得到重要性较高的10个因素按重要性排序分别为：
    
    甘油三酯、尿酸、尿素、天冬氨酸转换酶、谷氨酰基转换酶、红细胞平均体积、碱性磷酸酶、高密度脂蛋白胆固醇、肌酐、白细胞计数。

预测血糖值的均方误差为1.2。

### 存在的问题

1、对缺失值进行处理较为简单，仅仅是用均值进行填充；

2、使用的模型太简单，预测能力一般，对于异常的血糖值（明显高过正常值、或者明显低于正常值）预测能力较差；

3、均方误差较高，排名靠前的队伍的均方误差在0.8左右。

### 下一步工作

更为细致的处理缺失值，使用其它方法进行填充；选择其它的模型进行建模预测。