# mvrecmd 电影推荐系统，采用Item-Based协同过滤算法，实现了基本的电影推荐功能
[项目介绍文章](http://blog.taohuawu.club/article/item-based-movie-recommendation)
## 1. 系统模块
### 1.1 离线计算推荐电影模块
**本模块采用离线式计算推荐给每位用户的电影，采用Item-based算法并做了适当修改，主要分两部分:**

>1. 计算电影的相似度：利用调整的余弦相似度计算方法； 

>2. 相似度加权求和：使用用户已打分的电影的分数进行加权求和，权值为用户未打分的各电影与打分的各电影的相似度，然后对所有相似度的和求平均。

### 1.2 浏览推荐电影模块
该模块主要有三个功能:

>1. 按推荐指数降序排序显示推荐给每个用户的电影;

>2. 按分数和打分时间降序排序显示用户已打分的电影来和系统推荐给用户的电影进行对比;

>3. 浏览用户信息。
  
### 1.3 数据库设计模块  
  **由于数据量比较大，本系统将数据文件中的数据导入到mysql数据库中，来提高系统的性能，同时增加了一些额外数据表，来满足系统的要求。**
