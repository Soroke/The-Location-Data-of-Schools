# The-Location-Data-of-Schools-in-China
中国所有学校地理位置Json数据库（省市区地址，坐标）（分校区，大学，中学，小学等等）（Python爬虫）

基于项目[pg7go/The-Location-Data-of-Schools-in-China](https://github.com/pg7go/The-Location-Data-of-Schools-in-China)做了两个参数化

# 已收集数据（JSON格式）
* 所有学校（28610个，分校区，省市区，详细地址，坐标）  
* 所有学校（28610个，分校区，省市区）  
* 大学（8084个，分校区，省市区，详细地址，坐标）  
* 大学（8084个，分校区，省市区）  
# 数据来源  
百度地图API：http://lbsyun.baidu.com/index.php?title=webapi/guide/webservice-placeapi  
地区列表：https://github.com/modood/Administrative-divisions-of-China/blob/master/dist/areas.json  
# 前置依赖
Python Scrapy框架  
`pip install scrapy configparser`  
# 收集方法
## 修改config.ini
### 修改收集内容
将配置文件中的`type` 替换为相应内容 （学校/大学/中学/小学/幼儿园/培训班）
### 修改百度地图应用ak值
在百度控制台里面申请：http://lbsyun.baidu.com/apiconsole/key/create  
替换配置文件里的`ak_value`变量值

## 执行收集

执行如下命令开始收集
```
scrapy crawl spider
```
## 后续处理
dataHandle.py脚本  
可以按照自己的需求来筛选需要的内容，然后保存  



