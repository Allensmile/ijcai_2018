# ijcai_2018
      初赛第10名，复赛第16名解决方案，最终答辩的八支队伍之一
>最终比赛结果不太理想，没有进入top10.....<br>

>简单说下方案，训练数据用了7天的数据(去掉了6号的数据，因为转换率太低了)，特征大家都不会差太多，就不具体说了，转换率上午用的是去掉该记录所在的小时的剩余时间(上午)的转换率，下午就取上午的全部数据转换率，分作这几个特征来算转换率，用户的一些特征，商店商品的一些特征等等。<br>

>最终的融合是小组三个人模型的加权融合，最终成绩0.13907。<br>

>这是我第二次参赛了，总结下来的参赛的经验就是线下线上的逻辑需要一致，最典型的应用就是滑动窗口，参赛的朋友们都需要留意这个逻辑一致的问题，要想提高模型在线上的预测结果，就需要考虑你加的特征是否在全局数据上是逻辑一致的，比如在初赛的a榜的时候，线上的数据是进行了0.3抽样的，那么假如你要统计当天的相关的统计量就需要考虑到如何修正这个问题，在初赛的时候我对训练数据进行了采样取特征，这个trick让我在top10待了很久，更有意思的是换榜之后，我的成绩骤降到120多名，说明我的原有特征都很差，凭这个trick就可以做到还不错的效果；第二个需要留意的是特征选择，前期假如你凭自己拍脑袋加了很多特征，那么你往后面再加特征就不太会有改善，加特征就应该考虑其是否在训练数据与测试数据是同分布的。暂时就那么多，想到再更新。。。。<br>

 >搞了下腾讯的比赛，发现有sparse.hstack可以低成本空间存储高维稀疏的数据，ijcai没有用上。。。不然可以把属性，city等等都onehot了<br>
