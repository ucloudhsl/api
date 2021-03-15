# 获取cube的价格-GetCubePrice

获取cube的价格

# Request Parameters
|Parameter name|Type|Description|Required|
|---|---|---|---|
|Region|string|地域。 参见 [地域和可用区列表](https://docs.ucloud.cn/api/summary/regionlist)|**Yes**|
|Zone|string|可用区。参见 [可用区列表](https://docs.ucloud.cn/api/summary/regionlist)|**Yes**|
|ProjectId|string|项目ID。不填写为默认项目，子帐号必须填写。 请参考[GetProjectList接口](https://docs.ucloud.cn/api/summary/get_project_list)|No|
|Count|string|购买数量|**Yes**|
|Cpu|string|cpu配置|**Yes**|
|Mem|string|内存配置|**Yes**|
|ChargeType|string|计费模式。枚举值为： <br> > Year，按年付费； <br> > Month，按月付费；<br> > Dynamic，按小时预付费 <br> > Postpay，按秒后付费，默认为月付|No|
|Quantity|string|购买时长。默认:值 1。按小时购买（Dynamic/Postpay）时无需此参数。 月付时，此参数传0，代表购买至月末。|No|

# Response Elements
|Parameter name|Type|Description|Required|
|---|---|---|---|
|RetCode|int|返回码|**Yes**|
|Action|string|操作名称|**Yes**|
|Price|int||**Yes**|
|OriginalPrice|string||**Yes**|

# Request Example
```
https://api.ucloud.cn/?Action=GetCubePrice
&Region=cn-zj
&Zone=cn-zj-01
&ProjectId=WcYmOlWO
&Count=crmBHpsf
&Cpu=giPvbWun
&Mem=FSlShRcN
&ChargeType=YLtBxuvr
&Quantity=ILiBsGAn
```

# Response Example
```
{
    "Action": "GetCubePriceResponse", 
    "Price": 4, 
    "OriginalPrice": "FWYRdDnz", 
    "RetCode": 0
}
```

