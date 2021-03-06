# describeAudit


## 描述
查看当前实例已开启的审计选项。如当前实例未开启审计，则返回空<br>- 仅支持SQL Server

## 请求方式
GET

## 请求地址
https://rds.jdcloud-api.com/v1/regions/{regionId}/instances/{instanceId}/audit

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True| |地域代码，取值范围参见[《各地域及可用区对照表》](../Enum-Definitions/Regions-AZ.md)|
|**instanceId**|String|True| |RDS 实例ID，唯一标识一个RDS实例|

## 请求参数
无


## 返回参数
|名称|类型|描述|
|---|---|---|
|**result**|[Result](describeaudit#result)| |

### <div id="result">Result</div>
|名称|类型|描述|
|---|---|---|
|**enabled**|String[]| |

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|

## 请求示例
GET
```
public void testDescribeAudit(){
    DescribeAuditRequest request=new DescribeAuditRequest();
    request.setInstanceId("sqlserver-83uqv7avy4");
    request.setRegionId("cn-north-1");
    DescribeAuditResponse response= rdsClient.describeAudit(request);
    System.out.println(new Gson().toJson(response));
}

```

## 返回示例
```
{
    "requestId": "bpa2nb742v05wneqcdwrgbvu6pae5djf", 
    "result": {
        "enabled": [
            "DATABASE_OBJECT_ACCESS_GROUP"
        ]
    }
}
```
