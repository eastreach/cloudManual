### 权限模型

#### 账号权限
![permission.png](../images/permission.png)
1. CRS账号与PMS账号是独立的账号体系。
1. CRS账号绑定PMS账号后可拥有PMS中数据操作的权限。
1. CRS各终端登录时以CRS账号登录，CRS服务端负责鉴权。
1. 菜单权限分WEB控制台权限和移动端权限。
1. root为管理员账号，使用黑名单禁止权限，新增功能后默认拥有权限。
1. 非root为普通账号，使用白名单授权，需要管理员分配权限。

#### 功能权限。
1. kf_status: 房态修改权限。
1. kf_status_layer： 房态查看楼层限制，非空时过滤指定的楼层。
1. kf_status_yd： 客房预定，
1. kl_dcb： 康乐点菜宝，餐厅点餐。
1. kl_yd： 康乐预定，餐厅预定。
1. hotel_zd_paykind： 付款方式限制。
1. kl_order_revoke： 康乐订单撤销。

#### 移动端组织结构，扁平化菜单管理。
```
    public static final String RepJingYingNSumYingYeSum = "RepJingYingNSumYingYeSum";   //营业汇总
    public static final String RepJingYingNSumYingYe = "RepJingYingNSumYingYe";         //营业明细
    public static final String RepJingYingNSumShouKuanSum = "RepJingYingNSumShouKuanSum";         //收款汇总
    public static final String RepJingYingNSumShouKuan = "RepJingYingNSumShouKuan";         //收款明细
    public static final String KFMainRep = "KFMainRep";         //客房出租
    public static final String SpHSFaJIa = "SpHSFaJIa";         //房价分析
    public static final String SpJDJLRBKYFX = "SpJDJLRBKYFX";         //客源分析
    public static final String RepGetAnjyrbGuestKindXiao = "RepGetAnjyrbGuestKindXiao";         //客情分析
    public static final String KFMainRepDaily = "KFMainRepDaily";                       //出租率日报
    public static final String SpRepFrontSFFS = "SpRepFrontSFFS";                       //前台结算,实付发生
    public static final String SpRepFrontSFSX = "SpRepFrontSFSX";                       //前台发生,收付实现
    public static final String KFGetRoomAvailable = "KFGetRoomAvailable";               //可卖房
    public static final String KFGetRoomAllStatusSale = "KFGetRoomAllStatusSale";       //销售预订
    public static final String HotelZSR = "HotelZSR";         //总收入
    public static final String RepJingYingNSum = "RepJingYingNSum";         //日平衡
    public static final String AppLSWL = "AppLSWL";         //历史未来
    public static final String AppKLJY = "AppKLJY";         //康乐经营
    public static final String AppKLXY = "AppKLXY";         //康乐挂帐
    public static final String RepKLDC = "RepKLDC";         //康乐日平衡
    public static final String RepKFOrder = "RepKFOrder";                           //客房订单报表
    public static final String RepKLOrder = "RepKLOrder";                           //康乐订单报表
    //
    public static final String HGXDW = "HGXDW";                                     //协议客户
    public static final String KFRoom = "KFRoom";                                   //客房管理
    public static final String KFYD = "KFYD";                                       //客房预订
    public static final String KLPostCT = "KLPostCT";                               //餐厅管理
    public static final String KLCTYD = "KLCTYD";                                   //餐厅预订
    public static final String KLPostSN = "KLPostSN";                               //桑拿管理
    public static final String KLSNYD = "KLSNYD";                                   //桑拿预订
    public static final String AppointmentSpaces = "AppointmentSpaces";             //会场管理
    public static final String AppointmentDetail = "AppointmentDetail";             //会场预订
    public static final String KFInterface = "KFInterface";                         //客房接口
    public static final String KLOrder = "KLOrder";                           //康乐订单
    public static final String KFOrder = "KFOrder";                           //客房订单
    public static final String KLBillDetailTPCheck = "KLBillDetailTPCheck";         //单品核销
    public static final String KLBillDetailTPQuery = "KLBillDetailTPQuery";         //套票查询
    public static final String KFCTSelf = "KFCTSelf";                               //房餐券
    public static final String KLDCB = "KLDCB";                                     //康乐点菜宝
    public static final String SNTicket = "SNTicket";                               //桑拿取票
    public static final String SNSelfPay = "SNSelfPay";                             //桑拿结账
    public static final String KLOrderSC = "KLOrderSC";                             //康乐商城
```


#### WEB控制台组织结构
```
    public static final String GXDWContainer = "GXDWContainer";                               //会员中心
    public static final String YDContainer = "YDContainer";                               //预定中心
    public static final String OrderContainer = "OrderContainer";                               //订单中心
    public static final String SettingContainer = "SettingContainer";                               //设置中心
    public static final String ReportContainer = "ReportContainer";                               //报表中心
    public static final String HelpContainer = "HelpContainer";                                 //帮助中心
    //
    public static final String HGXDWContainer = "HGXDWContainer";                               //协议客户
    public static final String HotelZDActivityContainer = "HotelZDActivityContainer";           //营销活动
    public static final String KFYDContainer = "KFYDContainer";                         //客房预定
    public static final String KLYDContainer = "KLYDContainer";                         //康乐预定
    public static final String CRSKFOrderContainer = "CRSKFOrderContainer";             //客房订单
    public static final String CRSKLOrderContainer = "CRSKLOrderContainer";             //康乐订单
    public static final String HotelSettingContainer = "HotelSettingContainer";             //酒店设置
    public static final String KFSettingContainer = "KFSettingContainer";             //客房设置
    public static final String KLSettingContainer = "KLSettingContainer";             //康乐设置
    public static final String KCContainer = "KCContainer";             //库存设置
    public static final String KFInterfaceSettingContainer = "KFInterfaceSettingContainer";             //客房接口
    public static final String KLInterfaceSettingContainer = "KLInterfaceSettingContainer";             //康乐接口
    public static final String PluginSettingContainer = "PluginSettingContainer";             //组件模块
    public static final String WebSettingContainer = "WebSettingContainer";             //官网设置
    public static final String RepJingYingContainer = "RepJingYingContainer";             //经营收入
    public static final String RepKFContainer = "RepKFContainer";             //客房报表
    public static final String RepKLContainer = "RepKLContainer";             //康乐报表
    public static final String HotelDetailTransactionContainer = "HotelDetailTransactionContainer";             //支付流水
    public static final String RepContainer = "RepContainer";             //报表中心
    public static final String LogContainer = "LogContainer";             //日志中心
```