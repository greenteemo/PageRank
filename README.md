# PageRank
PageRank和TopicPageRank两种算法的简单实现

## python-graph-core
  通过该python库可构造图，模拟网页之间的链接关系

## PageRank
  代码实现主要参考[ref1: PageRank算法原理及实现](https://blog.csdn.net/rubinorth/article/details/52215036)  

## Topic PageRank
  逻辑上参考[ref2: Topic PageRank原理](https://blog.csdn.net/hguisu/article/details/8005192)

## main idea
  PageRank具体实现及逻辑可参考ref1。  
  在实现Topic PageRank时,多传入了一个topic_matrix的主题矩阵，其每一列（设该列表示主题：体育）表示所有网页（A,B,C,D）是否属于该主题，如属于则为1，反之为0。即若矩阵的某一列为[0,1,1,0]', 表示网页B,C属于该主题。
在测试效果时，假定用户的兴趣为体育0.6，音乐0.4，则将该用户兴趣向量[0.6,0.4]乘以topic_page_rank()返回的topic_rank矩阵最终得到的rank向量即为关于该用户的网页rank。

## 存在问题
  只能返回关于某用户的主题匹配的网页排序结果，而不是用户搜索关键字匹配的网页排序结果
