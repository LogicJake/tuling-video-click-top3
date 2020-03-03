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

