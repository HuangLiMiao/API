# API期末项目之交管助手
发布日期|2020-07-01
:--:|:--:
项目名称|交管助手
文件现状|在完成
文件的主人|黄丽妙
产品原型|[交管助手](https://76t0e1.axshare.com) |



# 项目名称： 交管助手
### 一、 MVP价值主张宣言
- 在日常生活中，传统的方式是交警看到违规的车辆，则现场执法、拍照或录像取证，最后抄写车牌贴条。然而交警开罚单要抄写车牌，这不仅容易出错，还会加大人力成本，并且时效性较差。有时候交警和车主之间还可能会发生一些冲突，因为有的车主会质疑自己被开罚单的公正性，从而引发两者之间的矛盾。基于现状，交管助手现将采用百度AI平台的车牌识别API、高德地图的定位识别API以及文字转语音API。交管助手可以通过交警输入的一张图片（可正常解码，且长宽比适宜），自动提取其车牌号以及定位，可以实时上报数据，并由系统自动判别该车辆是否违规停车，若违规后台系统将自动开罚单并打印，最后由后台机器人根据文字转化成语音打电话通知车主。
### 二、核心价值（最小可行性）
- 最小可行性产品：交警能一键拍照开罚单，节省时间和提高工作效率，减少开罚单的纠纷
### 三、问题表述与需求列表
#### 1.产品背景
- 随着现代化城市车辆的逐年剧增，车辆的大量增长同时也给交通管理带来了一定的麻烦，城市交通管理工作日趋复杂，而传统的交通执法已经无法满足现代化交通管理的需求，交管助手的出现能够助力于交警完成移动执法工作，为其提供执法的便利。

#### 2.用户画像
- 画像1
![用户画像1](https://github.com/HuangLiMiao/API/blob/master/imges/yonghu/yonghu1.PNG?raw=true)
- 画像2
![用户画像2](https://github.com/HuangLiMiao/API/blob/master/imges/yonghu/yonghu2.PNG?raw=true)
#### 3.需求列表

需求|用户场景|优先级|智能加值?|API类型
:--:|:--:|:--:|:--:|:--:
交警能够快速准确地开罚单|交警想高效地完成执勤工作，但手写开罚单难免有时会写错|重要|是|百度车牌识别API
交警能够快速地检查车辆是否违规|传统的执勤方式盘查到可疑车辆的时候都需要将其车牌信息、车辆外观、路段位置进行记录，再联系终端人员对比确认，步骤比较繁杂|重要|是|图片对比API 、高德地图位置识别API
交警开出的罚单具有公正性|传统的开罚单方式单凭执勤交警的个人判断，因此有些车主会质疑其公正性|次重要|否|高德地图位置识别API
交警及时联系违规停车车主开走违规停车车辆|传统的执勤方式需要将车牌信息传回信息中心才能找到车主信息，等待反馈时间较长|次重要|是|百度文字转语音API


#### 4.用户痛点
- 场景一：下雨天，交警外出执勤，写字很不方便
- 场景二：交警想要违规停车车主尽快回来移动车辆，不要妨碍交通
- 场景三：交警因被质疑开罚单是否公正与车主产生纠纷
- 场景四：交警被质疑违规执法给政府带来负面的影响


### [四、界面流程及关键智能交互](https://76t0e1.axshare.com)
- 界面流程图
![界面流程](https://github.com/HuangLiMiao/API/blob/master/imges/other/jiemian.jpg?raw=true)
- 产品原型图一览
![原型一览1](https://github.com/HuangLiMiao/API/blob/master/imges/yuanxing/yuanxing1.png?raw=true)
![原型一览2](https://github.com/HuangLiMiao/API/blob/master/imges/yuanxing/yuanxing2.png?raw=true)
![原型一览3](https://github.com/HuangLiMiao/API/blob/master/imges/yuanxing/yuanxing3.png?raw=true)

### 五、数据流程及关键智能API使用
- 数据流程图
![数据流程](https://github.com/HuangLiMiao/API/blob/master/imges/other/data.jpg?raw=true)
#### IDEO 三要素（论证 MVP 加/价值）
- Viability 商业可行性：自从公安部提出科技强警的政策方针以来，我国公安行业对切合一线警用的科研项目和设备投入了巨额经费。因此“云+端”的应用正在成为公安部门场景应用的常态,交管助手前景可观。
- Feasibility 技术可行性：借助百度API和高德API开放平台以实现产品主要技术，使用计算机视觉的智能视觉分析图像，并利用计算机智能文字转语音API。
- Desirability 用户可欲性：传统开罚单方式操作繁琐，且比较看交警个人主观判断，容易产生纠纷，此款产品不仅可以提高用户的工作效率，还可以比较客观公平地开罚单，从而减少相关的纠纷。

### [六、API 产品使用及输出展示](https://github.com/HuangLiMiao/API/blob/master/daima/finalwork.ipynb)
####（1）[百度车牌识别API])(https://ai.baidu.com/tech/ocr_cars/plate)
- 接口描述：支持识别中国大陆机动车蓝牌、黄牌（单双行）、绿牌、大型新能源（黄绿）、领使馆车牌、警牌、武警牌（单双行）、军牌（单双行）、港澳牌、农用车牌、民航车牌的地域编号和车牌号，并能同时识别图像中的多张车牌。
- [技术文档](https://ai.baidu.com/ai-doc/OCR/ck3h7y191)
- 调用示例
![result1](https://github.com/HuangLiMiao/API/blob/master/imges/result/result1.PNG?raw=true)

####（2）[高德地理编码API])(https://ai.baidu.com/tech/speech/tts_online)
- 接口描述：地理编码/逆地理编码 API 是通过 HTTP/HTTPS 协议访问远程服务的接口，提供结构化地址与经纬度之间的相互转化的能力。
- [技术文档](https://www.cnblogs.com/XieDong/p/7724556.html)
- 调用示例
![result2](https://github.com/HuangLiMiao/API/blob/master/imges/result/result2.PNG?raw=true)

####（3）[百度语音合成API])(https://ai.baidu.com/tech/speech/tts_online)
- 接口描述：百度语音合成服务，基于HTTP请求的REST API接口，将文本转换为可以播放的音频文件。合成的文件格式为 mp3，pcm（8k及16k），wav（16k），具体见aue参数。
- [技术文档](https://ai.baidu.com/ai-doc/SPEECH/Qk38y8lrl)
- 调用示例
![result3](https://github.com/HuangLiMiao/API/blob/master/imges/result/result3.PNG?raw=true)
