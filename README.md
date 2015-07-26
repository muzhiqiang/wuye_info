# 数据库文档

### _User 用户表

字段 | 类型 | 说明
:----------- | :-----------: | :----------:
objectId | String | 主键
name | String | 用户名
gender | String | 性别，格式：0 代表未知 1 代表男性 2 代表女性
age | Number | 年龄 
isMarried | Bool | 已婚否
email | String | 邮箱
houseId | Pointer | House 指针
password | String | 密码（哈希过）
occupation | String | 职业
username | String | 登录用户名
type | String | 用户类型，格式：owner 房东 tenant 租客
emailVerified | Bool | 邮箱是否验证
parkingId | Pointer | Parking 指针
mobilePhoneVerifield | Bool | 手机是否验证

### AdminManager 物业管理员表

字段 | 类型 | 说明
:----------- | :-----------: | :----------:
objectId | String | 主键
username | String | 用户名
password | String | 密码
villageId | Pointer | Village 指针

### Village 小区表

字段 | 类型 | 说明
:----------- | :-----------: | :----------:
objectId | String | 主键
name | String | 小区名
address | String | 具体地址
province | String | 省份，格式：广东省
city | String | 城市，格式：广州市

### Bill 账单表

字段 | 类型 | 说明
:----------- | :-----------: | :----------:
objectId | String | 主键
houseId | Pointer | House 指针
parkingId | Pointer | Parking 指针
year | Number | 年，格式：2015
month | Number | 月，格式：7
type | String | 类型，格式：水费、电费、停车费
unit | String | 单位，格式：吨、度、月
price | Number | 单价
total | Number | 总价
usage | Number | 用量
formula | String | 公式

### House 房屋表

字段 | 类型 | 说明
:----------- | :-----------: | :----------:
objectId | String | 主键
building | String | 座别
floor | String | 楼层
unit | String | 单元
villageId | Pointer | Village 指针

### Parking 停车位表

字段 | 类型 | 说明
:----------- | :-----------: | :----------:
objectId | String | 主键
building | String | 座别
floor | String | 楼层
unit | String | 单元
villageId | Pointer | Village 指针

### Notice 通知表

字段 | 类型 | 说明
:----------- | :-----------: | :----------:
objectId | String | 主键
title | String | 标题
content | String | 内容：xml 字符串
villageId | String | Village 指针
