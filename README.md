# API期末项目之交管助手
|  发布日期 | 2020-07-01 |
 | -- | -- |
 |  项目名称 | 交管助手 |
 |  文件现状 | 在完成 |
 |  文件的主人 | 黄丽妙 |
 | 产品原型 | [公正罚单](https://app.axure.cloud/app/project/76T0E1/overview) |



# 项目名称： 交管助手
### 一、 MVP价值主张宣言
- 在日常生活中，传统的方式是交警看到违规的车辆，则现场执法、拍照或录像取证，最后抄写车牌贴条。然而交警开罚单要抄写车牌，这不仅容易出错，还会加大人力成本，并且时效性较差。有时候交警和车主之间还可能会发生一些冲突，因为有的车主会质疑自己被开罚单的公正性，从而引发两者之间的矛盾。基于现状，交管助手现将采用百度AI平台的车牌识别API、高德地图的定位识别API以及文字转语音API。交管助手可以通过交警输入的一张图片（可正常解码，且长宽比适宜），自动提取其车牌号以及定位，可以实时上报数据，并由系统自动判别该车辆是否违规停车，若违规后台系统将自动开罚单并打印，最后由后台机器人根据文字转化成语音打电话通知车主。
### 二、核心价值（最小可行性）
- 最小可行性产品：交警能一键拍照开罚单，节省时间和提高工作效率，减少开罚单的纠纷
### 三、问题表述与需求列表
#### 1.产品背景
- 随着现代化城市车辆的逐年剧增，车辆的大量增长同时也给交通管理带来了一定的麻烦，城市交通管理工作日趋复杂，而传统的交通执法已经无法满足现代化交通管理的需求，交管助手的出现能够助力于交警完成移动执法工作，为其提供执法的便利。

#### 2.用户画像

#### 3.需求列表
| 需求 | 用户场景 | 优先级 | 智能加值？ |API类型 |
| :----: | :----: | :----: | :----: | :----: |
| 交警能够快速准确地开罚单 | 交警想高效地完成执勤工作，但手写开罚单难免有时会写错 | 重要 | 是 | 百度车牌识别API |
| 交警能够快速地检查车辆是否违规 | 传统的执勤方式盘查到可疑车辆的时候都需要将其车牌信息、车辆外观、路段位置进行记录，再联系终端人员对比确认，步骤比较繁杂 | 重要 | 是 | 图片对比API 、高德地图位置识别API |
| 交警开出的罚单具有公正性 | 传统的开罚单方式单凭执勤交警的个人判断，因此有些车主会质疑其公正性 | 次重要 | 否 | 高德地图位置识别API |
| 交警及时联系违规停车车主开走违规停车车辆 | 传统的执勤方式需要将车牌信息传回信息中心才能找到车主信息，等待反馈时间较长 | 次重要 | 是 | 百度文字转语音API |



#### 4.用户痛点
- 场景一：下雨天，交警外出执勤，写字很不方便
- 场景二：交警想要违规停车车主尽快回来移动车辆，不要妨碍交通
- 场景三：交警因被质疑开罚单是否公正与车主产生纠纷
- 场景四：交警被质疑违规执法给政府带来负面的影响
