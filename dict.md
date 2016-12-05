#简从系统数据库字典

（注：共45张表，按ctrl+F查找关键字）  
1. 表名：[sw_admin]      注释：后台用户表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | uid | int(10) |  | 主键（PRIMARY） | 
 | token | varchar(64) |  | 二次密码 | 
2. 表名：[sw_article]      注释：文章表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | mediumint(8) |  | 主键（PRIMARY） | 
 | title | varchar(128) |  | 文章标题 | 
 | message | text |  | 文章内容 | 
 | category_id | smallint(5) | 0 | 分类id | 
 | link | varchar(255) |  | 站外链接 | 
 | views | int(10) | 1 | 浏览量 | 
 | file_name | varchar(64) |  | 自定义文件名,默认为uuid | 
 | add_time | int(10) | 0 | 添加时间 | 
3. 表名：[sw_attach]      注释：附件表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(10) |  | 主键（PRIMARY） | 
 | uid | int(10) | 0 | 所属用户 | 
 | file_name | varchar(255) |  | 附件名称 | 
 | access_key | varchar(32) |  | access_key | 
 | add_time | int(10) | 0 | 添加时间 | 
 | file_location | varchar(255) |  | 本地文件路径 | 
 | file_size | int(11) | 0 | 文件大小 | 
 | item_type | varchar(32) |  | 附件所属类型 | 
 | item_id | int(11) | 0附件所属ID | 
 | file_type | varchar(16) |  | 文件类型 | 
 | is_image | tinyint(1) | 0 | 是否是图片 | 
 | attachment | varchar(255) |  | 缩略图 | 
 | thumbmin | varchar(255) |  | 小缩略图 | 
 | thumbmid | varchar(255) |  | 中缩略图 | 
4. 表名：[sw_buyer_activity]      注释：买家代言码激活表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | uid | int(11) | 0 | 使用者 | 
 | seller_uid | int(11) | 0 | 卖家 | 
 | add_time | int(11) |  | 添加时间 | 
 | end_time | int(11) | 0 | 过期时间 | 
5. 表名：[sw_buyer_code]      注释：买家代言码表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | uid | int(11) | 0 | 卖家 | 
 | code | varchar(16) |  | 买家使用码 | 
 | end_time | int(11) | 0 | 到期时间 | 
6. 表名：[sw_category]      注释：分类表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | smallint(5) |  | 主键（PRIMARY） | 
 | parent_id | smallint(5) | 0 | 父级分类 | 
 | title | varchar(64) |  | 分类标题 | 
 | description | varchar(255) |  | 描述 | 
 | icon | varchar(128) |  | 图标 | 
 | type | varchar(16) |  | 类型 | 
 | sort | smallint(5) | 0 | 排序 | 
 | file_name | varchar(64) |  | 分类别名 | 
7. 表名：[sw_feedback]      注释：意见反馈表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | mediumint(8) |  | 主键（PRIMARY） | 
 | uid | int(10) | 0 | 用户id | 
 | contact | varchar(32) |  | 联系方式 | 
 | message | text |  | 反馈内容 | 
 | has_reply | tinyint(1) | 0 | 是否已回复 | 
 | add_time | int(10) |  | 添加时间 | 
8. 表名：[sw_flow]      注释：订单流水表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | type | tinyint(2) | 0 | 资金流向，in1,out2 | 
 | action | tinyint(2) | 0 | 资金类型 | 
 | order_id | varchar(32) | 0 | 订单ID | 
 | user_name | varchar(64) |  | 用户名 | 
 | uid | int(10) | 0 | 用户id | 
 | product_id | int(10) |  | 产品id | 
 | item_id | int(10) |  | 产品套餐id | 
 | cash | int(10) |  | 金额,单位分 | 
 | user_balance | int(10) |  | 用户余额 | 
 | add_time | int(10) |  | 记录时间 | 
9. 表名：[sw_group]      注释：团购表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | product_id | int(11) | 0 | 产品id | 
 | status | varchar(16) |  | 状态,wait,close, ok | 
 | need_user | int(11) | 0 | 组团需要人数 | 
 | has_user | int(11) | 0 | 已经参加的人数 | 
 | add_time | int(11) | 0 | 开团时间 | 
 | uid | int(11) | 0 | 团长 | 
 | share_id | int(11) | 0 | 代言id | 
10. 表名：[sw_inbox]      注释：信息表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | uid | int(11) |  | 发送者 ID | 
 | dialog_id | int(11) |  | 对话id | 
 | message | text |  | 内容 | 
 | add_time | int(10) |  | 添加时间 | 
 | sender_remove | tinyint(1) | 0 | 发送者删除 | 
 | recipient_remove | tinyint(1) | 0 | 接受者删除 | 
 | receipt | int(10) | 0 | 接受者 | 
11. 表名：[sw_inbox_dialog]      注释：信息对话表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | sender_uid | int(11) |  | 发送者UID | 
 | sender_unread | int(11) |  | 发送者未读 | 
 | recipient_uid | int(11) |  | 接收者UID | 
 | recipient_unread | int(11) |  | 接收者未读 | 
 | add_time | int(11) |  | 添加时间 | 
 | update_time | int(11) |  | 最后更新时间 | 
 | sender_count | int(11) |  | 发送者显示对话条数 | 
 | recipient_count | int(11) |  | 接收者显示对话条数 | 
12. 表名：[sw_mobile_code]      注释：短信验证码表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | mobile | bigint(13) |  | 手机号 | 
 | code | mediumint(8) |  | 验证码 | 
 | status | tinyint(1) | 0 | 发送状态，0，未发送，1，已发送。 | 
 | add_time | int(10) |  | 添加时间 | 
13. 表名：[sw_notification]      注释：通知表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | sender_uid | int(10) | 0 | 发送通知者 | 
 | recipient_uid | int(10) | 0 | 接收通知者 | 
 | action_type | smallint(6) | 0 | 通知类型 | 
 | add_time | int(10) | 0 | 添加时间 | 
 | read_flag | tinyint(1) | 0 | 阅读状态 | 
 | data | text |  | 内容 | 
14. 表名：[sw_order]      注释：订购表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(10) |  | 主键（PRIMARY） | 
 | uid | int(10) | 0 | 订购用户 | 
 | cash | int(10) | 0 | ,金额，单位：分 | 
 | add_time | int(10) | 0 | 下单时间 | 
 | note | varchar(255) |  | 买家留言 | 
 | payment_order_id | varchar(32) | 0 | 订单id | 
 | pay_time | int(10) | 0 | 支付时间 | 
 | product_id | int(10) | 0 | 产品id | 
 | item_id | int(10) | 0 | 产品套餐id | 
 | amount | smallint(5) | 0 | 购买数量 | 
 | address_id | int(10) | 0 | 收货地址id | 
 | pay_way | varchar(16) |  | 支付方式，alipay,weixin | 
 | status | varchar(16) | wait | 状态，close,关闭，wait,等待付款，ok,已经付款，sending,正在发货，success，成功 | 
 | spread_uid | int(10) | 0 | 推广者 | 
 | share_id | int(10) | 0 | 来自哪个分享id | 
 | express_company | varchar(64) |  | 快递公司 | 
 | express_code | varchar(32) |  | 快递单号 | 
 | send_time | int(10) | 0 | 发货时间 | 
 | success_time | int(10) | 0 | 确认收货时间 | 
 | seller_uid | int(10) | 0 | 卖家uid | 
 | has_send_msg | tinyint(1) | 0 | 是否已经下发通知 | 
 | order_status | tinyint(2) | 0 | 订单状态。 | 
 | spread_percent | smallint(3) | 0 | 下单时产品的推广分成。 | 
 | real_name | varchar(64) |  | 收货姓名 | 
 | province | varchar(16) |  | 省份 | 
 | city | varchar(16) |  | 城市 | 
 | county | varchar(16) |  | 县、区 | 
 | address | varchar(255) |  | 详细地址 | 
 | mobile | bigint(13) |  | 收货人手机号 | 
 | postcode | mediumint(8) |  | 邮编 | 
 | extra | text |  | 附加字段 | 
 | group_id | int(11) | 0 | 团购id | 
15. 表名：[sw_order_extra]      注释：订购附加字段表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | product_id | int(11) | 0 | 产品id | 
 | extra_name | varchar(45) |  | 附件字段名称 | 
 | is_need | tinyint(1) | 0 | 是否必填 | 
 | error_tip | varchar(45) |  | 错误提示 | 
 | default_tip | varchar(45) |  | 默认提示 | 
 | listorder | int(11) | 0 | 排序 | 
16. 表名：[sw_order_refund]      注释：退款订单处理表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | order_id | varchar(32) |  | orderid | 
 | refund_cash | int(11) | 0 | 退款金额，单位分 | 
 | add_time | int(11) | 0 | 申请时间 | 
 | end_time | int(11) | 0 | 处理结束时间 | 
 | status | tinyint(1) | 0 | 退款状态 | 
 | refund_type | varchar(255) |  | 退款类型 | 
 | note | text |  | 退款说明 | 
 | refund_time | int(11) | 0 | 商家驳回时间 | 
 | agree_time | int(11) | 0 | 同意退款时间 | 
17. 表名：[sw_order_refund_data]      注释：退款详情表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | refund_id | int(11) | 0 | 退款id | 
 | uid | int(11) |  | 用户 | 
 | user_type | tinyint(4) | 0 | 用户类型 | 
 | add_time | int(11) | 0 | 添加时间 | 
 | message | text |  | 协商详情 | 
 | status | tinyint(1) | 0 | 状态,1同意,2拒绝,驳回 | 
18. 表名：[sw_payment]      注释：付款表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(10) |  | 主键（PRIMARY） | 
 | order_id | varchar(32) | 0 | 订单id | 
 | uid | int(10) | 0 | 付款用户 | 
 | cash | int(10) | 0 | 付款金额 | 
 | add_time | int(10) | 0 | 添加时间 | 
 | note | varchar(255) |  | 附加信息 | 
 | terrace_id | varchar(64) |  | 交易号 | 
 | type | varchar(16) |  | 支付类型 | 
 | pay_time | int(10) | 0 | 付款时间 | 
19. 表名：[sw_product]      注释：产品表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(10) |  | 主键（PRIMARY） | 
 | title | varchar(255) |  | 产品标题 | 
 | message | longtext |  | 产品详情 | 
 | uid | int(10) | 0 | 卖家ID | 
 | category_id | smallint(5) | 0 | 分类id | 
 | has_attach | tinyint(1) | 0 | 是否有附件 | 
 | add_time | int(10) | 0 | 添加时间 | 
 | views | int(10) | 1 | 浏览量 | 
 | share_count | int(11) | 0 | 分享次数 | 
 | order_money | int(11) | 0 | 售出金额 | 
 | order_count | mediumint(8) | 0 | 订购次数 | 
 | is_recommend | tinyint(1) | 0 | 是否推荐 | 
 | news_count | smallint(5) | 0 | 新闻动态 | 
 | item_count | smallint(5) | 0 | 项目数量 | 
 | status | tinyint(2) | 1 | 状态,0，审核，1，正常，2，下架 | 
 | file_name | varchar(36) |  | 自定义文件名 | 
 | thumb | varchar(255) |  | 缩略图 | 
 | postage | varchar(255) |  | 邮费 | 
 | title_fulltext | text |  | 标题索引 | 
 | spread_percent | smallint(2) | 10 | 推广收益百分比，默认是10% | 
 | start_time | int(11) | 0 | 活动开始时间 | 
 | end_time | int(11) | 0 | 活动结束时间 | 
 | share_default_text | text |  | 代言预设 | 
 | group_need_user | int(11) | 0 | 团购多少人成团 | 
20. 表名：[sw_product_item]      注释：产品套餐表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(10) |  | 主键（PRIMARY） | 
 | product_id | int(10) | 0 | 产品id | 
 | title | varchar(255) |  | 套餐名称 | 
 | price | float(10,2) | 0.00 | 套餐价格,单位元 | 
 | icon | varchar(255) |  | 图标 | 
 | add_time | int(10) |  | 添加时间 | 
 | amount | int(10) |  | 数量限制，0或为空则为999 | 
 | rest_amount | int(10) | 0 | 剩余数量 | 
 | user_limit | smallint(5) | 0 | 限制购买数量 | 
 | order_count | mediumint(8) |  | 已订购数量 | 
 | listorder | smallint(5) |  | 排序 | 
 | group_price | float(10,2) | 0.00 | 团购价格 | 
21. 表名：[sw_product_news]      注释：产品动态表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | uid | int(10) | 0 | 用户id | 
 | product_id | int(10) | 0 | 产品id | 
 | message | text |  | 动态内容 | 
 | has_attach | tinyint(1) | 0 | 是否有附件 | 
 | add_time | int(10) | 0 | 添加时间 | 
 | comment_count | smallint(5) | 0 | 评论数量 | 
22. 表名：[sw_product_news_comment]      注释：产品动态评论表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(10) |  | 主键（PRIMARY） | 
 | uid | int(10) | 0 | 用户id | 
 | news_id | int(10) | 0 | 产品动态id | 
 | message | text |  | 评论内容 | 
 | at_uid | int(10) | 0 | 提到的用户 | 
 | add_time | int(10) | 0 | 添加时间 | 
23. 表名：[sw_product_share]      注释：产品代言表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | uid | int(10) | 0 | 代言用户 | 
 | product_id | int(10) | 0 | 产品id | 
 | message | text |  | 代言内容 | 
 | add_time | int(10) | 0 | 添加时间 | 
 | has_attach | tinyint(1) | 0 | 是否有附件 | 
 | order_count | int(10) | 0 | 通过我的分享订购了多少 | 
 | parent_id | int(11) | 0 | 父级分享id | 
 | votes | int(11) | 0 | 点赞数量 | 
 | comments | int(11) | 0 | 评论数量 | 
 | is_recommend | tinyint(1) | 0 | 是否推荐 | 
24. 表名：[sw_product_tags]      注释：产品简介
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | product_id | int(11) | 0 | 产品id | 
 | tag_name | varchar(255) |  | 标签名称 | 
 | tag_value | varchar(255) |  | 标签内容 | 
 | listorder | int(11) | 0 | 排序 | 
25. 表名：[sw_session]      注释：session内存表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | char(32) |  | 主键（PRIMARY） | 
 | uid | int(10) | 0 |  | 
 | mobile | bigint(13) | 0 |  | 
 | ip | bigint(12) | 0 |  | 
 | last_activity | int(10) | 0 |  | 
 | life_time | int(10) | 0 |  | 
26. 表名：[sw_setting]      注释：系统设置表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | smallint(6) |  | 主键（PRIMARY） | 
 | varname | varchar(32) |  | 变量名称 | 
 | varvalue | text |  | 变量值 | 
27. 表名：[sw_share_comment]      注释：代言评论表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | share_id | int(11) | 0 | 代言id | 
 | uid | int(11) | 0 | 用户id | 
 | message | text |  | 评论内容 | 
 | add_time | int(11) | 0 | 添加时间 | 
 | at_uid | int(11) | 0 | 提到的用户id | 
28. 表名：[sw_share_vote]      注释：代言赞记录表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | uid | int(11) | 0 | uid | 
 | share_id | int(11) |  | 代言id | 
 | rating | tinyint(1) | 0 | 赞同 | 
 | add_time | int(11) |  | 添加时间 | 
29. 表名：[sw_user]      注释：用户表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | uid | int(10) |  | 主键（PRIMARY） | 
 | user_name | varchar(64) |  | 用户名 | 
 | mobile | bigint(13) | 0 | 手机 | 
 | password | varchar(64) |  | 密码 | 
 | avatar | varchar(128) |  | 头像 | 
 | balance | bigint(14) | 0 | 用户余额，单位：分 | 
 | add_time | int(10) | 0 | 加入时间 | 
 | reg_ip | bigint(12) | 0 | 注册ip | 
 | last_activity | int(10) |  | 最后一次活动时间 | 
 | product_count | smallint(6) | 0 | 产品数量 | 
 | share_count | smallint(6) | 0 | 代言数量 | 
 | status | tinyint(1) | 1 | 0,审核，1正常，-1，封禁 | 
 | notification_unread | int(10) | 0 | 未读通知 | 
 | verified | tinyint(1) | 0 | 认证状态，0未认证，1认证商家，2,实名认证 | 
 | introduction | varchar(255) |  | 简介 | 
 | inbox_unread | int(10) | 0 | 未读消息 | 
 | votes | int(11) | 0 | 点赞数 | 
 | comments | int(11) | 0 | 评论数 | 
 | contact | varchar(32) |  | 联系方式 | 
 | weixin_qrcode | varchar(255) |  | 微信二维码 | 
30. 表名：[sw_user_account]      注释：收款账号表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(10) |  | 主键（PRIMARY） | 
 | uid | int(10) | 0 | 用户id | 
 | type | varchar(16) |  | 账号类型 | 
 | real_name | varchar(64) |  | 真实姓名 | 
 | account | varchar(64) |  | 账号 | 
 | is_index | tinyint(1) | 0 | 默认 | 
31. 表名：[sw_user_address]      注释：收货地址表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(10) |  | 主键（PRIMARY） | 
 | uid | int(10) | 0 | 用户id | 
 | real_name | varchar(64) |  | 收货人 | 
 | province | varchar(16) |  | 省份 | 
 | city | varchar(16) |  | 城市 | 
 | county | varchar(16) |  | 县、区 | 
 | address | varchar(255) |  | 详细地址 | 
 | mobile | bigint(13) | 0 | 收货人手机号 | 
 | postcode | mediumint(8) | 0 | 邮政编码 | 
 | is_index | tinyint(1) | 0 | 默认地址 | 
32. 表名：[sw_user_comment]      注释：卖家评论表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | author_uid | int(11) | 0 | 卖家id | 
 | uid | int(11) | 0 | 评论用户id | 
 | message | text |  | 评论内容 | 
 | add_time | int(11) | 0 | 添加时间 | 
 | at_uid | int(11) | 0 | 提到的用户 | 
33. 表名：[sw_user_follow]      注释：卖家关注表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | fans_uid | int(11) |  | 关注人的UID | 
 | friend_uid | int(11) |  | 被关注人的uid | 
 | add_time | int(10) |  | 添加时间 | 
34. 表名：[sw_user_qq]      注释：QQ绑定表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | bigint(12) unsigned |  | 主键（PRIMARY） | 
 | uid | int(11) |  | 用户id | 
 | nickname | varchar(64) |  | qq昵称 | 
 | openid | varchar(128) |  | openid | 
 | gender | varchar(8) |  | 性别 | 
 | add_time | int(10) |  | 添加时间 | 
 | access_token | varchar(64) |  | access_token | 
 | refresh_token | varchar(64) |  | refresh_token | 
 | expires_time | int(10) |  | 有效期 | 
 | figureurl | varchar(255) |  | 头像地址 | 
35. 表名：[sw_user_vote]      注释：卖家赞表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | uid | int(11) | 0 | uid | 
 | author_uid | int(11) |  | 帮主id | 
 | rating | tinyint(1) | 0 | 赞同 | 
 | add_time | int(11) |  | 添加时间 | 
36. 表名：[sw_user_weixin]      注释：微信绑定表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(10) |  | 主键（PRIMARY） | 
 | uid | int(10) | 0 | 用户id | 
 | openid | varchar(32) |  | openid | 
 | expires_in | int(10) |  | 有效期 | 
 | access_token | tinytext |  | access_token | 
 | refresh_token | tinytext |  | refresh_token | 
 | scope | varchar(64) |  | scope | 
 | headimgurl | varchar(255) |  | 头像地址 | 
 | nickname | varchar(64) |  | 微信昵称 | 
 | province | varchar(32) |  | 省份 | 
 | city | varchar(32) |  | 城市 | 
 | add_time | int(11) | 0 | 添加时间 | 
 | has_download | tinyint(1) | 0 | 是否已经下载头像，crond | 
37. 表名：[sw_verify]      注释：认证表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | uid | int(11) |  | 用户id | 
 | reason | varchar(255) |  | 申请原因 | 
 | add_time | int(11) |  | 添加时间 | 
 | contact | varchar(32) |  | 联系方式 | 
 | logo | varchar(255) |  | 认证头像 | 
 | weixin_qrcode | varchar(255) |  | 微信二维码 | 
 | name | varchar(64) |  | 认证名称 | 
38. 表名：[sw_verify_apply]      注释：认证申请表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | uid | int(10) | 0 |  | 
 | reason | varchar(255) |  | 原因 | 
 | attach | varchar(255) |  | 附件 | 
 | add_time | int(11) |  | 提交时间 | 
 | name | varchar(255) |  | 认证名称 | 
 | data | text |  | 认证内容 | 
 | status | tinyint(1) | 0 | 状态，0等待，-1未通过，1通过 | 
 | type | tinyint(1) | 0 | 认证类型，1，商家认证，2个人认证 | 
 | logo | varchar(255) |  | 认证头像 | 
 | weixin_qrcode | varchar(255) |  | 客服微信二维码 | 
39. 表名：[sw_weixin_crond]      注释：微信消息发送计划任务表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | openid | varchar(64) |  | openid | 
 | content | text |  | 格式化的内容 | 
 | link | varchar(255) |  | 链接 | 
 | has_send | tinyint(1) | 0 | 是否发送了 | 
 | title | varchar(255) |  | 消息标题 | 
40. 表名：[sw_weixin_login]      注释：微信登录表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(10) |  | 主键（PRIMARY） | 
 | token | int(10) |  | token | 
 | uid | int(10) |  | 登录的用户id | 
 | session_id | varchar(32) |  | session_id | 
 | expire | int(10) | 0 | 有效期 | 
41. 表名：[sw_weixin_message]      注释：微信消息表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(11) |  | 主键（PRIMARY） | 
 | weixin_id | varchar(64) |  | openid | 
 | content | varchar(255) |  | 消息内容 | 
 | action | text |  | 消息类型 | 
 | time | int(10) | 0 | 发送时间 | 
 | reply_message | text |  | 回复的消息内容 | 
 | has_reply | tinyint(2) | 0 | 是否已回复 | 
42. 表名：[sw_weixin_msg]      注释：微信群发列表,未用到
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(10) |  | 主键（PRIMARY） | 
 | msg_id | bigint(20) |  |  | 
 | group_name | varchar(255) | 未分组 |  | 
 | status | varchar(15) | unsent |  | 
 | error_num | int(10) |  |  | 
 | main_msg | text |  |  | 
 | articles_info | text |  |  | 
 | questions_info | text |  |  | 
 | create_time | int(10) |  |  | 
 | filter_count | int(10) | 0 |  | 
43. 表名：[sw_weixin_qr_code]      注释：微信二维码,未用到
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | scene_id | mediumint(5) |  | 主键（PRIMARY） | 
 | ticket | varchar(255) |  |  | 
 | description | varchar(255) |  |  | 
 | subscribe_num | int(10) | 0 |  | 
44. 表名：[sw_weixin_reply_rule]      注释：微信自动回复规则表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(10) |  | 主键（PRIMARY） | 
 | account_id | int(10) | 0 | 值1 | 
 | keyword | varchar(255) |  | 关键词 | 
 | title | varchar(255) |  | 回复内容 | 
 | image_file | varchar(255) |  | 图片地址 | 
 | description | text |  | 图片描述 | 
 | link | varchar(255) |  | 链接地址 | 
 | enabled | tinyint(1) | 0 | 是否启用 | 
 | sort_status | int(10) | 0 |  | 
45. 表名：[sw_withdraw]      注释：用户提现表
 | 字段 | 类型 | 默认 | 注释 | 
 | --------- | --------- | --------- | --------- | 
 | id | int(10) |  | 主键（PRIMARY） | 
 | uid | int(10) | 0 | 用户id | 
 | cash | int(10) | 0 | 提现金额 | 
 | real_cash | int(10) | 0 | 真正的金额 | 
 | type | varchar(16) |  | 提现到哪里 | 
 | real_name | varchar(64) |  | 真实姓名 | 
 | account | varchar(64) |  | 提现到的账号 | 
 | add_time | int(10) | 0 | 申请时间 | 
 | pay_time | int(10) | 0 | 支付时间 | 
 | order_id | varchar(32) | 0 | 订单id | 
 | terrace_id | varchar(64) |  | 微信、支付宝返回的支付流水号 | 
 | note | varchar(255) |  | 附加信息 | 
 | status | varchar(16) | wait | 状态 | 
 | last_time | int(11) | 0 | 最后一次请求提现接口时间 | 
 | times | smallint(5) | 0 | 请求提现接口次数 | 
