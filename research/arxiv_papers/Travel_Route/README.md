# 项目介绍

基于贪婪算法的路线规划问题旨在确定在给定起点和终点之间的最优或接近最优路线。本文首先采用主成分分析（PCA）方法对城市评价指标进行降维，以提取关键主成分。接着，利用KMO算法和TOPSIS算法对数据进行进一步降维，这些算法均基于MindSpore框架实现。对于未通过KMO检验的数据集，我们将采用熵权法和TOPSIS法进行综合评价。在贪婪算法的基础上，我们提出并优化了路线规划算法，以满足游客的不同需求，提供个性化的路线定制。此外，为了降低成本并避免陷入局部最优解，我们还考虑了当地的旅行效率、游览景点所需的时间以及每天必要的休息时间。



本文已经发表在arxiv上
《Research on Travel Route Planing Problems Based on Greedy Algorithm》 https://arxiv.org/abs/2410.13226

如需要引用可以用如下格式：
 Yiquan Wang. Research on Travel Route Planing Problems Based on Greedy Algorithm *arXiv preprint arXiv:2410.13226*



实验结果基于MindSpore框架得出，特别感谢MindSpore社区的支持。

数据集来源如下：

1.华为云OBS：https://travelroute.obs.cn-east-3.myhuaweicloud.com/travel_route_data.zip

2.个人GitHub：https://github.com/wyqmath/RoutePlaning_GreedyAlgorithm



本项目的灵感来源于第五届”华数杯“数学建模大赛。

代码的简介如下：

### Q1

我们的初步工作是对数据集进行了初步加工，这一阶段的重点包括游玩时长、票价、营业时间等核心数据的处理。通过运用正则表达式及逻辑判断技巧，我们有效地进行了格式标准化和信息完善。

### Q2

在深入分析“外国游客最想参观的50个城市”时，我们采取了一套严谨而系统的研究方法。首先，通过KMO测试验证了数据的适合性，确保后续分析的有效基础。随后，运用主成分分析（PCA）技术，我们成功地对复杂多样的城市指标进行了降维处理，提炼出影响游客偏好的关键主成分，既简化了问题又保留了关键信息。

紧接着，我们采用了基于熵权法的TOPSIS模型，这一方法充分利用了各指标数据的不确定性信息来确定其权重，确保了权重分配的客观性和合理性。在综合考虑了城市规模、环境魅力、人文底蕴、交通便利性、气候条件以及美食文化等全方位因素后，我们构建了一个多维度的评价体系。通过TOPSIS方法，我们在多个评价标准下进行了细致的对比与排序，最终科学地筛选并排序出了“最受外国游客喜爱的50个城市”名单。

### Q3

针对始发于广州的旅客，本研究提出了一项利用高速铁路进行交通优化的旅行规划方法。该模型中纳入了总的时间约束、各旅游点所需的参观时间以及门票费用。利用贪心算法，模型能够在限定的时间内规划出访问尽可能多高评价景点的理想路线。此外，该规划方案不只是简单地考虑高铁的行程时间，还综合考量了各景区内部移动所需时间及旅客每日的休息需求，以保证方案的现实可行性和逻辑性。

### Q4

本研究旨在实现游历更多城市的同时，尽量降低旅游中门票与交通的总开支。通过对景点的评级与花费进行全面分析，本研究找到了一种均衡策略，确保游客在有限的预算内能享受到最优质的旅行体验。

### Q5

我们将重点关注偏好山景的游客，在352个城市里，我们精心挑选出所有与山景有关的风光。然后，我们通过综合评价和路径规划，为旅客打造了一条在144小时内能欣赏到最高评分山景的最优旅行路线。。此种个性化的规划途径不仅适用于山景游，也能扩展到其他主题旅行，如美食体验、文化探寻等。

