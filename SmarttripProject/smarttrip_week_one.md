## 智慧旅游项目数据调研报告

### 一、前言

本次调研报告主要是对实验室智慧旅游项目的数据进行调查研究，总体分为数据的横向调研和纵向调研。数据的横向调研旨在为下一步爬取新类型的数据提供指导；数据的纵向调研则是分析当前数据库中已有数据的字段。

### 二、数据横向调研

为了真正了解用户在旅游问答中的需求，本次调研从用户提出的关于海南旅游的问题着手，爬取了携程旅游问答板块关于关键字“海南”的所有问题。

根据爬取到的旅游问题，本次调研进一步对问答进行了分析，爬取问答板块数据保存为"HainanQA.txt"（问题标题数据文件）和"HainanQAinfo.txt"（问题内容数据文件），通过文本挖掘分析出问答板块的词频。

问题标题数据的词频分析结果为：

```
(spider) ➜  ctripQASpider git:(master) ✗ python source/extractWords.py
Building prefix dict from the default dictionary ...
Loading model from cache /var/folders/2w/lx69b5fd0fxb62qv7lzctmlh0000gn/T/jieba.cache
Loading model cost 1.053 seconds.
Prefix dict has been built succesfully.
['海南', '酒店', '请问', '度假', '上海', '三亚', '南站', '上海南京东路', '外滩', '怎么', '上海南京路', '可以', '什么', '步行街', '机场', '泳池', '君澜', '别墅', '地铁站', '海口']
```

问题内容数据的词频分析结果为：

```
(spider) ➜  ctripQASpider git:(master) ✗ python source/extractWords.py
Building prefix dict from the default dictionary ...
Loading model from cache /var/folders/2w/lx69b5fd0fxb62qv7lzctmlh0000gn/T/jieba.cache
Loading model cost 1.024 seconds.
Prefix dict has been built succesfully.
['海南', '三亚', '谢谢', '酒店', '请问', '南站', '上海', '回复', '大家', '海口', '什么', '等待', '景点', '怎么', '机场', '推荐', '美食', '哪里', '可以', '旅游']
```

根据结果不难发现，酒店、景点、美食等词汇出现在旅游问答的高频词汇中，也揭露了用户在外出海南旅游时更关心食、住、玩方面；同时，南站、机场、地铁站等字眼也表明了用户还会询问一些交通数据，步行街词汇的出现则预示着用户提问购物方面问题的可能；

尽管问答分析仅爬取了携程上的1000条问题，数据无法概括整体，但是也足以为下一步数据爬取提供一些思路。

未来爬取数据的一些想法和安排：

1. 酒店数据：
    
    现在各大网站平台上酒店的数据繁多，可供爬取的网站有[艺龙旅行][]、[携程旅行][]、[飞猪旅行][]，还有一些民宿网站，例如[爱彼迎][]，具体爬取网站根据后续网站爬取难易程度和数据质量决定；
    
2. 交通数据：
    
    对于交通方面的数据，初步打算尝试爬取一些机票数据，还有在知乎上了解一下爬取公交线路数据和公交站点数据的解决方案；
    
3. 购物数据：
    
    对于购物方面，可以爬取[马蜂窝][]和[途牛][]网站上一些购物中心的数据，还可以爬取海南的离岛免税的购物网站（[三亚国际免税城官方商城][]和[免税易购][]
），海南建设国际旅游岛，同时，推出了离岛免税政策，所以来海南玩的游客应该也会问询一些离岛免税购物的问题；

4. 攻略数据：
    
    虽然上述的问答词频分析没有体现出攻略数据的价值，但是对于自由行游客来说，游客还是时常在出行前了解旅游攻略和制定出行计划，而[马蜂窝][]网站上有大量的游记数据，可供我们爬取。
    
    
    
[艺龙旅行]: http://hotel.elong.com/haikou/

[携程旅行]: https://hotels.ctrip.com/hotel/haikou42#ctm_ref=hod_hp_sb_lst

[飞猪旅行]: https://hotel.fliggy.com/hotel_list3.htm?cityName=%BA%A3%BF%DA&city=460100&keywords=&checkIn=2018-09-09&checkOut=2018-09-10

[爱彼迎]: https://zh.airbnb.com/s/%E6%B5%B7%E5%8F%A3/homes?refinement_paths%5B%5D=%2Fhomes&query=%E6%B5%B7%E5%8F%A3&allow_override%5B%5D=&s_tag=VPChgL51****

[三亚国际免税城官方商城]: https://www.baidu.com/link?url=wTjzOzxUPPZo3T3IDmJswXPU0CHgdtA5s8SHDE1Ad9_csL_eHZZ421SpvQ4gP-8b&ck=7102.3.9999.347.146.351.156.5&shh=www.baidu.com&sht=baidu&wd=&eqid=d820faf5000211e1000000065b90a617

[免税易购]: https://www.baidu.com/link?url=A0wnv-xaa-VKKuxZI6XucPeX0u9b5tyQ-2z-H2VeojSEZRGF0zb9rTd7V6hz05mo&ck=6001.4.9999.313.398.351.156.7&shh=www.baidu.com&sht=baidu&wd=&eqid=d820faf5000211e1000000065b90a617

[马蜂窝]: http://www.mafengwo.cn/

[途牛]: http://www.tuniu.com/g900/shopping-0-0/s41/1/

### 三、数据纵向调研

智慧旅游数据的纵向调研主要是通过询问师兄师姐数据的使用情况来进行的，目的在于发现已有数据格式上的不足以及已有数据的缺陷。根据师兄师姐的反馈，主要有以下问题：

1. 饭店数据和景点数据的地区字段areaName有所不同，由于饭店数据取自美团，美团对地区的划分细致到行政地区，乃至商圈，而景点数据取自马蜂窝，对地区的划分只是到市县级别，所以在进行问答时，用户问完“龙华区有哪些好吃的？”，之后可能会问到“龙华区有哪些好玩的景点”，这时问答机器人就无法根据数据回答用户问题了；
2. 景点数据还有一个缺陷在于，缺少一些景点游玩的团购信息，或者套票信息，只给出了简单的门票信息，同时，经过师兄师姐的提醒，景点数据还缺乏评分字段，由于缺乏景点的评分，无法通过评分来推荐景点给用户，还需要进一步补足景点数据；
