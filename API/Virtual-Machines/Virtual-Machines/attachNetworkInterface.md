# attachNetworkInterface


## 描述
云主机绑定一块弹性网卡。<br>
云主机状态必须为<b>running</b>或<b>stopped</b>状态，并且没有正在进行中的任务才可操作。<br>
弹性网卡上如果绑定了弹性公网IP，那么其所在az需要与云主机的az保持一致，或者为全可用区型弹性公网IP，才可挂载该网卡。<br>
云主机挂载弹性网卡的数量，不能超过实例规格的限制。可查询<a href="http://docs.jdcloud.com/virtual-machines/api/describeinstancetypes">DescribeInstanceTypes</a>接口获得指定规格可挂载弹性网卡的数量上限。<br>
弹性网卡与云主机必须在相同vpc下。


## 请求方式
POST

## 请求地址
https://vm.jdcloud-api.com/v1/regions/{regionId}/instances/{instanceId}:attachNetworkInterface

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True| |地域ID|
|**instanceId**|String|True| |云主机ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**networkInterfaceId**|String|True| |弹性网卡ID|
|**autoDelete**|Boolean|False| |随云主机删除而自动删除，默认为False|


## 返回参数
无


## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**400**|Invalid parameter|
|**401**|Authentication failed|
|**404**|Not found|
|**500**|Internal server error|
|**503**|Service unavailable|
