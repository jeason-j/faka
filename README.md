# faka

源码来源于网上  演示网站 https://faka.ssrsu.com

20190809更新 增加新的支付对接




以下是源码自带的说明：
最简易的个人发卡网站
演示站运行环境：win2008系统 + php5.3

安装方法1：将源码上传至根目录，运行/install按提示进行安装(强烈建议)

安装方法2：将源码上传至根目录，手工导入数据库kami.sql后，修改config.php配置信息

后台地址：你的域名/tb888   用户名和登陆密码都是admin    安全密码：aa6688

特别注意：安装好后一定要修改后台路径，用户名和2个密码！

          安全密码修改：tb888/ajax.php文件中17行


此源码已对接ABC支付接口+码支付接口

接口申请无需任何资料，ABC支付接口申请地址：http://pay.sddyun.cn/user/reg.php

                      码支付接口申请地址：https://codepay.fateqq.com/


ABC支付接口修改下面两个文件:

other/submit.php   51行   修改成你自己的商户ID

other/epay/epay.config.php    修改成你自己的商户ID和商户密钥


码支付接口修改下面两个文件:

other1/submit.php   24和25行   修改成你自己的码支付ID和通信密钥

other1/codepay_return.php   14行  修改成你自己的通信密钥


两个接口如何切换：

现在源码默认的是ABC支付接口，如果切换成码支付的，修改js/ayangw.js 第95行

window.location.href ="other/submit.php?"+u;  这个是ABC云支付的

window.location.href ="other1/submit.php?"+u;  这个是码支付的

注：更改后如果没有切换，刷新一下你的网址/js/ayangw.js这个文件，是缓存问题


提醒：以上文件千万不要使用记事本修改，推荐使用DW8等专用编辑工具


有人会问为什么不把支付接口弄到后台？那样设置还方便，回答是你方便了，黑客也方便了！

这样操作在服务器外是不可能被恶意修改支付接口导致资金损失的！
