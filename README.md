# 2016-2017赛季NBA常规赛结果预测
## 项目简介
我是NBA的狂热粉，从2003年姚明刚进入NBA的时候就开始关注NBA，从小玩到大的游戏也是NBA，从早期的NBAlive到现在的NBA2K。  
我喜欢看NBA比赛，也爱看NBA各项数据，既然学了这么久数据分析，那么也是时候和我的另一个爱好NBA相结合，来分析下NBA数据。  
本次项目将基于2015-2016年的NBA 常规赛及季后赛的比赛统计数据，预测2016-2017常规赛每场赛事的结果。  
由于影响比赛胜负的因素较多，本次分析将不考虑16-17赛季将发生的球员交易、球员伤病、教练变动等影响因素，仅基于15-16的赛季状态来分析。
## 数据来源
本次用于分析的数据来源于专门统计NBA各项数据的Basketball Reference.com网站，用于分析的主要分四个表格：Team Per Game Stats，每支球队平均每场比赛的表现统计；Opponent Per Game Stats，每支球队所遇到的对手平均每场比赛的统计信息；Miscellaneous Stats，每支球队综合统计数据；NBA Schedule and Results，赛季日历和结果。以上数据都是15-16赛季的数据。还有用于预测的16-17Schedule也就是16-17赛季赛程表，在分析过程中发现16-17赛季比赛日历少了森林狼和开拓者的比赛，所以自己补上了。
## 公式引用
 **Elo Score**: Elo等级分最初为了提供国际象棋中，更好地对不同的选手进行等级划分。在现在很多的竞技运动或者游戏中都会采取 Elo 等级分制度对选手或玩家进行等级划分，如足球、篮球、棒球比赛或 LOL，DOTA 等游戏。  
 **E(A)**: A 对 B 的胜率期望值,E(A)=1/(1+10^((Elo(B)-Elo(A))/400)  
 **E(B)**: B 对 A 的胜率期望值,E(B)=1/(1+10^((Elo(A)-Elo(B))/400)  
 **更新Elo Score**: 如果 A 在比赛中的真实得分 S(A)(胜 1 分,和 0.5 分,负 0 分)和他的胜率期望值 E(A)不同，  
 则他的等级分要根据以下公式进行调整：Elo<sup>new</sup>(A)=Elo<sup>old</sup>(A)+K(S(A)-E(A)),根据等级分的不同 K 值也会做相应的调整。 