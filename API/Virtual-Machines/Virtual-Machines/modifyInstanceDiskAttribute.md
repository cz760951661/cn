# modifyInstanceDiskAttribute


## 描述
修改云主机挂载的数据盘属性，包括是否随主机删除。<br>
仅按配置计费云硬盘支持设置随实例删除属性;包年包月计费云硬盘该属性不生效,实例删除时云硬盘将保留。<br>


## 请求方式
POST

## 请求地址
https://vm.jdcloud-api.com/v1/regions/{regionId}/instances/{instanceId}:modifyInstanceDiskAttribute

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True| |地域ID|
|**instanceId**|String|True| |云主机ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**dataDisks**|[InstanceDiskAttribute[]](modifyinstancediskattribute#instancediskattribute)|False| |云硬盘列表|

### <div id="instancediskattribute">InstanceDiskAttribute</div>
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**diskId**|String|False| |云硬盘ID|
|**autoDelete**|Boolean|False| |随云主机一起删除，删除主机时自动删除此磁盘，默认为false，本地盘(local)不能更改此值。<br>如果云主机中的数据盘(cloud)是包年包月计费方式，此参数不生效。<br>如果云主机中的数据盘(cloud)是共享型数据盘，此参数不生效。<br>|

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
