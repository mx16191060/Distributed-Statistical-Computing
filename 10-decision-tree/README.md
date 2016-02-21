# 实例分析：术后病人安置方案的决策树模型


## 准备知识

* 决策树模型
* Python和Spark






###数据预处理



### 建立决策树

将已转化成 LabeledPoint 格式的数据集 data 分成 3:1 的两份,一份为训练集

	(trainingData, testData) = data.randomSplit([0.75, 0.25]) ###生成训练集和测试集 
	Model = DecisionTree.trainClassifier(trainingData, numClasses=3,\ 			categoricalFeaturesInfo={}, impurity='gini', maxDepth=5, maxBins=32)

### 在测试集上预测


（感谢北京大学魏诗韵提供素材和案例。）