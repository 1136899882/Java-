使用通配符
在执行SQL对象之前，必须调用相应的方法设置通配符？代表具体的值
如： sql.setFloat(1,1.76f);
     sql.setString()
     
     
     
     
     
     
     
     String str = "select * from mess where height < ? and name = ?"
     PreparedStatement sql = con.prepareStatement(str);
     
     
     
     随即流
      使用RandomAccessFile类来创建一个随机访问的文件流，创建的流指向既可以作为源也可以作为目的地
       构造方法
       
       
       
       try{ inAndOut = new RandomAccessFile("","rw");
       for(int i =0; i<data.length;i++){
       }
       }




2.sigmoid函数:



3.假设的含义：



4.性质：



5.找一个凸损失函数



6.可由最大似然估计推导出

单个样本正确预测的概率为



只是3两个式子合并在一起的表示方法

整个样本空间的概率分布为



取对数展开得，



作为损失函数，并且最小化它，则应改写为5式。

7.求解方法

最原始的方法，梯度下降法

先求导，并带入sigmoid表达式得



之后，参数更新为：



终止条件：

目前指定迭代次数。后续会谈到更多判断收敛和确定迭代终点的方法。

8.高级方法

共轭梯度

BFGS,L-BFGS

9 Advanced optimization(其他优化算法)

优化算法：

给定参数θ，我们可以写成代码来计算：

逻辑回归优化算法-我爱公开课-52opencourse.com

优化算法除了梯度下降算法外，还包括：

Conjugate gradient method(共轭梯度法)
Quasi-Newton method(拟牛顿法)
BFGS method
L-BFGS(Limited-memory BFGS)
后二者由拟牛顿法引申出来，与梯度下降算法相比，这些算法的优点是：

第一，不需要手动的选择步长；

第二，通常比梯度下降算法快；

但是缺点是更复杂-更复杂也是缺点吗？其实也算不上，关于这些优化算法，推荐有兴趣的同学看看52nlp上这个系列的文章：无约束最优化，作者是我的师兄，更深入的了解可以参考这篇文章中推荐的两本书：

用于解无约束优化算法的Quasi-Newton Method中的LBFGS算法到这里总算初步介绍完了，不过这里笔者要承认的是这篇文档省略了许多内容，包括算法收敛性的证明以及收敛速度证明等许多内容。因此读者若希望对这一块有一个更深入的认识可以参考以下两本书：
1) Numerical Methods for Unconstrained Optimization and Nonlinear Equations（J.E. Dennis Jr. Robert B. Schnabel）
2) Numerical Optimization（Jorge Nocedal Stephen J. Wright）

7) Multi-class classification: One-vs-all(多类分类问题)

多类分类问题举例：

电子邮件分类/标注： 工作邮件，朋友邮件，家庭邮件，爱好邮件

医疗图表(medical diagrams): 没有生病，着凉，流感

天气：晴天，多云，雨，雪

二类分类问题如下图所示：

二类分类问题-我爱公开课-52opencourse.com

多类分类问题如下所示：

多类分类问题-我爱公开课-52opencourse.com

One-vs-all(one-vs-rest):

对于多类分类问题，可以将其看做成二类分类问题：保留其中的一类，剩下的作为另一类。例如，对于下面这个例子：

多分类问题-one-vs-all-我爱公开课-52opencourse.com

可以分别计算其中一类相对于其他类的概率：

one-vs-rest-多分类问题-我爱公开课-52opencourse.com

总结-One-vs-all方法框架：

对于每一个类 i 训练一个逻辑回归模型的分类器h(i)θ(x)，并且预测 y = i时的概率；

对于一个新的输入变量x, 分别对每一个类进行预测，取概率最大的那个类作为分类结果：

多分类问题预测-我爱公开课-52opencourse.com

 



       
     
