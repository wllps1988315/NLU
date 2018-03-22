假设你是投资公司的分析师,分析跟踪航空股(airline stocks).
假设有一个任务,分析航空公告增长和后边一天股票增幅的关系.
股票价格的历史数据很容易得到,但航空公告是不是容易得到呢?
首先得知道航空的名称,提出加价的本质,公告日期,其他航空可能的反应.
这些都能在新闻文章中得到,比如下面的新闻:<br>

Citing high fuel prices, United Airlines said Friday it has increased fares by $6 per round trip on flights to some cities also
served by lower- cost carriers. American Airlines, a unit of AMR Corp., immediately matched the move, spokesman Tim Wagner said.
United, a unit of UAL Corp., said the increase took effect Thursday and applies to most routes where it competes against discount
carriers, such as Chicago to Dallas and Denver to San Francisco.


信息抽取(information extraction):信息抽取(IE)把未结构化文本结构化,比如关系数据库的补充.

命名实体识别(named entity recognition):IE第一步是在文本中抽取正确的名称或者命名实体.
命名实体的任务是发现文本中mention的命名实体,给命名实体打标签和类型.
特定的应用程序有特定的命名实体类型,通常有人名,地名,组织名;
也有特殊的命名实体类型,比如大学课程中基因和蛋白质的名字.

文本中定位命名实体后,进行link,cluster聚类,比如推断出United Airlines 和United是同一个实体.
共指消解部分会详细讲解这部分内容.

关系抽取(relation extraction):关系抽取的任务是发现实体间的语义分类关系,通常都是二元关系,
比如spouse-of,child-of,employment,part-whole,membership和geospatial relations(地理空间关系).

关系抽取与填充关系数据库有着密切的联系。

事件抽取(event extraction):事件抽取的任务是发现实体参与的时间,比如,United和American票价增长.
同事也需要找到event coreference,弄清事件是否为同一个事件;在上边示例中,increase和the move指的是同一个事件.

时间表示(temporal expression):为了弄清楚事件发生的时间,我们需要弄清楚时间表示(temporal expression),
比如Friday,months,holidays等,时间段(relative expressions),比如two days from now,next year,3:30,noon.
时间归一化(temporal expression normalization)是指把temporal expressions映射到具体的日期,或者事件对应的时间.
本文例子中,Friday指美联航宣布的时间(time of United’s announcement),
Thursday指票价增长的日期,产生一个时间序列(timeline),
美联航宣布(United’s announcement)在票价增长之后(fare increase),美国的公告(American’s announcement)在两者事件之后.

模板填充(template filling):很多文本表述形式都比较固定.模板填充(template filling)的任务就是发现这种固定句式,用正确的形式填充句式.
槽填充内容源自于文本,分词后进行抽取,比如时间(times),数量(amounts),本体实体(ontology entities).
![](./pic/槽模板.png)
