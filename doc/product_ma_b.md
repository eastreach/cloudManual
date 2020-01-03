### 小程序【瑞通云】
![product_ma_b](../images/product_ma_b.jpg)

#### 扫码跳转指定页面设置。
1. 前缀在小程序申请成功后由系统分配。
1. 路由参数由管理员进行设置。
1. 扫码点餐 
    ```
    http://crs.eastreach.com/ma/b/wxaccd06f101c5b60d?action=KLPostCTDC&hotelId=bjklrqdjd&client=21&code=201
    ```
    ![扫码点餐](../images/KLPostCTDC_bjklrqdjd_21_201.png)
    
#### 小程序授权部署流程
1. 设置中心-微信开放平台-菜单管理：授权接入，小程序管理员扫码授权给瑞通。
#### 小程序支付配置，同主体的商户号。
1. 产品中心，appId授权，添加小程序的appid。
. 账户中心，API安全，设置API密钥，提交商户号和API密钥（大小写，字母数字）。
1. 产品中心，开发配置，JSAPI授权目录: http://api.eastreach.com/
1. 如果需要退款： 账户中心，API安全，下载API证书。
