# tuling-video-click-top3
图灵联邦视频点击预测大赛线上第三

# 2020-TURING-TOPIA-Video-Click-SINGLE-LightGBM-top3
===============================================================================================================     
**图灵联邦视频点击预测大赛线上第三（LightGBM单模）**
## 主办方： 图灵联邦
## 赛道：2020-视频点击预测大赛

**赛道链接**：https://www.turingtopia.com/competitionnew/detail/e4880352b6ef4f9f8f28e8f98498dbc4/sketch       
**赛程时间**：*2019.11.11-2020.03.09*  
**参与人**：[第一次打比赛](https://github.com/LogicJake)、[郑](https://github.com/jackhuntcn) 、[小兔子乖乖](https://github.com/PandasCute) 、   [Freak](https://github.com/PandasCute)   
**方案文档**：[文档链接](https://www.logicjake.xyz/2020/02/10/%E5%9B%BE%E7%81%B5%E8%81%94%E9%82%A6%E8%A7%86%E9%A2%91%E7%82%B9%E5%87%BB%E9%A2%84%E6%B5%8B%E5%A4%A7%E8%B5%9B-%E8%B5%9B%E5%90%8E%E6%80%BB%E7%BB%93/)      
**百度云盘下载链接**:为避免数据丢失，提供数据集下载地址链接: https://pan.baidu.com/s/1YPtg4QyiAdhRAMoxjis_Gw  密码: 0a3r       
## 1.数据说明  
**train.csv**

| 字段     | 中文名| 数据类型|  说明 |
|:-------:|:-------:|:-------:|:-------:|
|id|	用户ID|	VARCHAR2(50)|	代表数据集的第几条数据，从1到11376681|
|target|	是否点击|	VARCHAR2(50)|	代表该视频是否被用户点击了，1代表点击，0代表未点击。|
|timestamp|修改时间戳|	VARCHAR2(50)|代表改用户点击改视频的时间戳，如果未点击则为NULL。|
|deviceid|	设备ID|	VARCHAR2(50)|用户的设备id|
|newsid|视频ID|	VARCHAR2(50)|视频的id。|
|guid|注册ID|	VARCHAR2(50)|	用户的注册id。|
|pos|推荐位置|	VARCHAR2(50)|	视频推荐位置|
|app_version|app版本|	VARCHAR2(50)|	app版本。|
|device_vendor|设备厂商|	VARCHAR2(50)|	设备厂商|
|netmodel|网络类型|	VARCHAR2(50)|	网络类型。|
|osversion|操作系统版本|	VARCHAR2(50)|	操作系统版本。|
|lng|经度|	VARCHAR2(50)|经度。|
|lat|维度|	VARCHAR2(50)|	维度。|
|device_version|设备版本|	VARCHAR2(50)|	设备版本。|
|ts|	用户ID|时间戳|	视频暴光给用户的时间戳。|

**test.csv**

| 字段     | 中文名| 数据类型|  说明 |
|:-------:|:-------:|:-------:|:-------:|
|id|	用户ID|	VARCHAR2(50)|	test_1到test_3653592|
|deviceid|	设备ID|	VARCHAR2(50)|用户的设备id|
|newsid|视频ID|	VARCHAR2(50)|视频的id。|
|guid|注册ID|	VARCHAR2(50)|	用户的注册id。|
|pos|推荐位置|	VARCHAR2(50)|	视频推荐位置|
|app_version|app版本|	VARCHAR2(50)|	app版本。|
|device_vendor|设备厂商|	VARCHAR2(50)|	设备厂商|
|netmodel|网络类型|	VARCHAR2(50)|	网络类型。|
|osversion|操作系统版本|	VARCHAR2(50)|	操作系统版本。|
|lng|经度|	VARCHAR2(50)|经度。|
|lat|维度|	VARCHAR2(50)|	维度。|
|device_version|设备版本|	VARCHAR2(50)|	设备版本。|
|ts|	用户ID|时间戳|	视频暴光给用户的时间戳。|

**app.csv**

| 字段     | 中文名| 数据类型|  说明 |
|:-------:|:-------:|:-------:|:-------:|
|id|	用户ID|	VARCHAR2(50)|	test_1到test_3653592|
|**deviceid**|	设备ID|	VARCHAR2(50)|用户的设备id|
|applist deviceid|视频ID|	VARCHAR2(50)|用户所拥有的app，我们已将app的名字设置成了app_1,app_2..的形式。|

**test.csv**

| 字段     | 中文名| 数据类型|  说明 |
|:-------:|:-------:|:-------:|:-------:|
|id|	用户ID|	VARCHAR2(50)|	test_1到test_3653592|
|deviceid|	设备ID|	VARCHAR2(50)|用户的设备id|
|guid|注册ID|	VARCHAR2(50)|	用户的注册id。|
|outertag|用户画像|	VARCHAR2(50)|用户画像用竖号分隔，冒号后面的数字代表对该标签的符合程度，分数越高代表该标签越符合该用户。|
|tag|用户画像|	VARCHAR2(50)|同outertag|
|level|用户等级|	VARCHAR2(50)|用户等级。|
|personidentification|是否优劣|	VARCHAR2(50)|1表示劣质用户 0表示正常用户。|
|followscore|徒弟分|	VARCHAR2(50)|徒弟分（好友分）。 |
|personalscore|个人分|	VARCHAR2(50)|个人分。 |
|gender|性别|	VARCHAR2(50)|性别|

## 2.配置环境与依赖库 
  - python3
  - scikit-learn
  - gensim
  - Ubuntu   
  - LightGBM
  - notebook 
## 3.运行代码步骤说明  
分别按照代码顺序  
运行1,2,3,4 
> 1 feature.ipynb	 特征工程 
> 2 fold_model.ipynb	    
> 3 offline_model.ipynb 离线模型  
> 4 online_model.ipynb 线上模型 

## 4.特征工程      
 - **原始特征**     
 - **穿越特征**   
 - **统计特征** 
 - **embedding特征**     
## 5.模型训练   
单模，初赛最终榜：0.83695 线上第三

