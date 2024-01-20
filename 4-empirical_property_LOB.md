# Empirical Properties of Limit Order Books

## Summary Statistics

如下是对四个股票的订单流和LOB的统计分析数据

<img src="/Users/tanzeren/Library/Application Support/typora-user-images/截屏2024-01-19 21.32.01.png" alt="截屏2024-01-19 21.32.01" style="zoom:33%;" />

可以总结出以下信息：

-   日换手大约都在0.5%左右，
-   LOB中在中间价附近1%内的量占日交易量的1%-3%
-   低价股在最优队列上发生的秒级以下交易比高价股多的多（表格中后两列对应的是低价股，即所谓large-tick stock）
-   高价股中发生的能吃掉第一档的市价单比低价股多一个数量级

## Intra-day pattern

### 市场行为分布

<img src="/Users/tanzeren/Library/Application Support/typora-user-images/截屏2024-01-19 21.49.03.png" alt="截屏2024-01-19 21.49.03" style="zoom:33%;" />

开盘时和快收盘时市场时最活跃的，一个可能的解释是：

-   开盘时市场在消化前一天收盘后到开盘时的市场信息
-   收盘时之前没有完成交易的交易者需要尽快完成交易
-   市场中中低频交易者的增加

并且高价股和低价股并没有明显的差异

<img src="/Users/tanzeren/Library/Application Support/typora-user-images/截屏2024-01-19 21.53.31.png" alt="截屏2024-01-19 21.53.31" style="zoom:33%;" />

观察最优档位的挂单量可以发现，对于高价股，挂单量是J-shaped，但是低价股开盘时量很少，收盘时急剧增加。

<img src="/Users/tanzeren/Library/Application Support/typora-user-images/截屏2024-01-19 21.56.53.png" alt="截屏2024-01-19 21.56.53" style="zoom:33%;" />

高价股和低价股的spread分布也体现出了明显差异，低价股的spread绝对值很小。并且有一个有意思的现象：

-   开盘时的spread明显比之后的大。

## Spread Distribution

<img src="/Users/tanzeren/Library/Application Support/typora-user-images/截屏2024-01-19 22.00.30.png" alt="截屏2024-01-19 22.00.30" style="zoom:50%;" />

低价股的spread大多数时候是一个tick，高价股的spread则更大，随着spread增大，概率近似于指数衰减

## **Order Arrivals and Cancellations**

<img src="/Users/tanzeren/Library/Application Support/typora-user-images/截屏2024-01-19 22.11.40.png" alt="截屏2024-01-19 22.11.40" style="zoom:33%;" />

上图画出的是限价单的下单价格和当时的本方最优价之间的距离的分布，可以看到在最优价挂单的最多。随着离最优价距离越深，概率逐渐减少。对于低价股（上半部分），下降几乎是单调的，但是对于高价股，在离最优价差不多一个spread的地方还有一个概率较大的峰值点，这可能说明按照spread划分价格是一个可行的方法。

## **Order Size Distributions**

<img src="/Users/tanzeren/Library/Application Support/typora-user-images/截屏2024-01-19 22.23.25.png" alt="截屏2024-01-19 22.23.25" style="zoom:50%;" />

订单大小的分布很广泛，尾部概率和power law近似

## **Volume at the Best Quotes**

<img src="/Users/tanzeren/Library/Application Support/typora-user-images/截屏2024-01-19 22.42.27.png" alt="截屏2024-01-19 22.42.27" style="zoom:25%;" />

形状和钱一张图类似，但是区别在于前一张图中量小的地方概率较大，但是在这张图中概率在小量处的聚集性没有那么明显，因为最优档位往往是由很多个订单共同组成的，所以量会比单个订单更大。

## Volume Profiles

<img src="/Users/tanzeren/Library/Application Support/typora-user-images/截屏2024-01-20 13.24.45.png" alt="截屏2024-01-20 13.24.45" style="zoom:25%;" />

可以发现在离对手方最优价很远的地方，也就是很深的档位依然有很多挂单，同时挂单的价格有round-number effect，参与者倾向于挂单在离对手方最优1,1.5,2,2.5的地方。

## **Tick-Size Effects**

<img src="/Users/tanzeren/Library/Application Support/typora-user-images/截屏2024-01-20 13.36.54.png" alt="截屏2024-01-20 13.36.54" style="zoom:25%;" />

spread和price是近似于线性的，但是因为spread不小于0.01，所以当price很小的时候，spread等于0.01

<img src="/Users/tanzeren/Library/Application Support/typora-user-images/截屏2024-01-20 13.38.25.png" alt="截屏2024-01-20 13.38.25" style="zoom:25%;" />

上图横轴为relative tick size即0.01/mid_price, 纵轴为最优档位上的量/每天的成交量，可以发现高价股最优档位的量占日成交量比例大约不到1%，但是低价股可以到10%。

<img src="/Users/tanzeren/Library/Application Support/typora-user-images/截屏2024-01-20 13.42.26.png" alt="截屏2024-01-20 13.42.26" style="zoom:25%;" />

上图是市价单的大小相对于最优档量的占比随着relative tick size的变化。低价股市价单的量占最优档量通常比较小，不到10%，但是对于高价股这个比例可能会大于1（图中画出的是平均值的相除）。



Reference:

