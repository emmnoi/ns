	开放网络服务信息收集实验
		alexa全球排名top 10000的站点选择其一
		禁止使用任何方式直接扫描目标站点
		禁止对目标站点进行任何形式的渗透测试或攻击行为
		信息收集手段包括但不限于：搜索引擎搜索、whois查询、域名枚举、使用合法客户端连接目标端口等
		信息收集内容包括但不限于：子域名及其对应服务说明、IP地址段、电子邮件、组织结构信息、联系方式信息、公开的漏洞信息等



目标站点：www.jd.com
=================================


![](http://i.imgur.com/hQXuXrh.png)

		1、目标站点服务器ip：106.39.178.1
		2、TTL=52   ——〉目标主机使用的是LINUX系统
		3、64-52+1=13   经过了13个节点
		4、目标主机是在线的

![](http://i.imgur.com/0UQKrf9.png)

		通过tracert命令可以得到从我的主机到达目标主机经过的路径
		现在来分析一下上面的路由结果：
		第一列：经过的节点数
		第二、三、四列：各节点的响应时间（每次发送三个探测包）
		第五列：经过的路由器ip

		域名：jd.com  
		注册商：MARKMONITOR INC.
		联系人：domain admin     
		联系方式：     whois反查
		更新时间：2015年10月13日
		创建时间：1992年09月29日
		过期时间：2024年03月08日
		域名服务器：whois.markmonitor.com
		DNS服务器：NS1.JDCACHE.COM
		DNS服务器：NS2.JDCACHE.COM
		DNS服务器：NS3.JDCACHE.COM
		DNS服务器：NS4.JDCACHE.COM
		域名状态：运营商设置了客户禁止删除保护 http://www.icann.org/epp#运营商设置了客户禁止删除保护
		域名状态：运营商设置了客户禁止转移保护 http://www.icann.org/epp#运营商设置了客户禁止转移保护
		域名状态：运营商设置了客户禁止修改保护 http://www.icann.org/epp#运营商设置了客户禁止修改保护
		域名状态：域名服务器上禁止删除保护 http://www.icann.org/epp#域名服务器上禁止删除保护
		域名状态：域名服务器上禁止转移保护 http://www.icann.org/epp#域名服务器上禁止转移保护
		域名状态：域名服务器上禁止修改保护 http://www.icann.org/epp#域名服务器上禁止修改保护
		
		    
		 源域名：360buy.com
    		2013年3月启用新域名：jd.com
		(来源：中国互联网络信息中心http://www.cnnic.com.cn)

# ip地址所在地（来源：查站网http://www.siteloop.net/subhost/jd.com)
![](http://i.imgur.com/NrCsvvo.png)
![](http://i.imgur.com/xwn7w49.png)

# 近7天百度指数（来源：百度指数查找页面http://index.baidu.com)
![](http://i.imgur.com/gIASGXz.png)

# 2014年网购投诉情况：（来源：315电子消费投诉网）
![](http://i.imgur.com/1bnKqZj.png)

#京东2015年业绩（来源：新华网）

    交易总额（GMV）达人民币878亿元，同比增长99%，达到行业平均增速的2倍*以上。

    实现净收入人民币366亿元，同比增长62%。

    年度活跃用户数在截至2015年3月31日的12个月期间达到1.052亿，同比增长90%。

    完成订单量达到2.272亿，同比增长76%。

    移动端渠道完成订单量约占总完成订单量的42%，同比劲增329%。


# 端口分析：  
**收集手段：** whois 查询   
**网站地址：**     
**收集内容：**    
![](http://i.imgur.com/2vN13lc.png)  
		开放端口有80和443  
		HTTP服务器默认的端口号为80  
		HTTPS服务器默认端口443  

**风险分析：**如果攻击者知道网站的某些开放端口，那么攻击者可以利用某些端口扫描的技术进行抓包，对该网站的主机或网络设备进行探测。比如开放扫描 ，会产生大量审计数据，容易被对方发现，但其可靠性高。隐蔽扫描 ：能有效避免对方侵检测系统和防火强墙的检测，但这种扫描使用的数据包在通过网络时容易被丢弃，从而产生错误的探测信息。另外也可以通过一些特殊的Ping命令对目标主机产生大量的数据包从而使目标主机反应不过来，达到了使网站暂时拒绝服务的目的。针对80端口常用的利用方式：lls溢出/SQL注入/旁注/跨站。443是能够提供加密以及通过安全端口传输的http.京东是一个交易型网站，所以很有必要开启443端口保证网页安全性。但是如果黑客利用SSL漏洞进行攻击的话可以盗取用户的信用卡账号登陆账号等。   
**风险级别：** 高。     
**后果：**设备信息泄露，发现网站漏洞，用户账号泄露，网站拒绝服务。    
**措施：**关闭闲置端口，安装可靠的防火墙。    

# SE0综合查询：
**收集手段：**whois  
**网站地址：**  [http://seo.chinaz.com/](http://seo.chinaz.com/)
**收集内容：**  
1.网站基本信息  
![](http://i.imgur.com/CfsHHh2.png)

2.百度相关  
![](http://i.imgur.com/R5a1hKm.png)  

3.各浏览器收录信息  
![](http://i.imgur.com/UHQnRIY.png)  

4.相关关键词在各浏览器上的排名  
![](http://i.imgur.com/95jqo5F.png)    

5.服务器信息
![](http://i.imgur.com/3TtF0rt.png)

# 官方备案信息 
**收集手段：**京东主页面给出的官方备案信息  
**收集内容：**  
![](http://i.imgur.com/NCNI1OL.png)

反馈信息：
------------------------------------------------------------
有以上关于京东的基本信息可以得出，京东在世界网站中排名都是十分靠前的，并且在百度首页中处于第一的位置，百度流量将近100万，说明京东使用人数庞大，每天的点击量也是不断增长。通过在百度、谷歌、360、搜狗几个浏览器的对比，我们可以看出，京东在百度中的收录数量是最多的，远远多于其他浏览器。另外，相关关键词在各浏览器中的排名也明显的突出了京东的特点，京东的主要商品是数码电子产品，手机，电脑和笔记本在搜索量上远远超过其他产品。




		京东注册邮箱：jdym@jd.com  使用该邮箱的注册人还有以下
		- 域名	              注册人
		- 1000xun.com	      周 永跃
		- 12306ng.cn	      北京京东世纪贸易有限公司
		- 12306ng.org	      zhang yan
		- 3.cn	              北京京东叁佰陆拾度电子商务有限公司
		- 360buy.biz	      liu qiang dong
		- 360buy.com	      domain admin
		- 360buy.net	      zhang yan
		- 360buyad.com	      zhang yan
		- 360buycdn.com	      yan zhang
		- 360buyimg.com     	周 永跃
		- 360by.com	         liuqiangdong
		- 360jd.com.cn	      北京京东世纪贸易有限公司
		- 360smart.com.cn	  刘强东
		- 500ccc.com	      zhang yan
		- baitiao.cn	      北京京东叁佰陆拾度电子商务有限公司
		- chouke.com.cn	      北京京东叁佰陆拾度电子商务有限公司
		- dao123.com	      zhangyan
		- daojiajd.com	      yan zhang
		- dongdong.com	      zhang yan
		- egouwang.com	      liuqiangdong
		- fight11.com	      zhang yan
		- fight618.com	      zhang yan
		- imok.com.cn	      腾讯科技(深圳)有限公司
		- jd.cc	domain        admin
		- jd.com	          domain admin
		- jd.hk	              邮件      jdym@jd.com
		- jd.ren	          zhang yan
		- jd.wang	          zhang yan
		- jd360.hk	          邮件 jdym@jd.com
		- jd-app.com	      zhang yan
		- jdb2b.com	          zhang yan
		- jdbao.com.cn	      北京京东世纪贸易有限公司
		- jdbao.net.cn	      北京京东世纪贸易有限公司
		- jdcache.com	      zhang yan
		- jdcdn.com         	周 永跃
		- jddj.com	          zhang yan
		- jd-ex.com	          yan zhang
		- jdjinrong.com     	zhang yan
		- jdlaser.com	       xiaoli zhai
		- jdos.cn	          北京京东世纪贸易有限公司
		- jdshop.cn	          北京京东叁佰陆拾度电子商务有限公司
		- jingdog.cn	      北京京东叁佰陆拾度电子商务有限公司
		- jingdog.net.cn	  北京京东叁佰陆拾度电子商务有限公司
		- jingdong.cx	      xiaoli zhai
		- jingdong.wang     	zhang yan
		- jingdongdaojia.com	zhang yan
		- jingdongshangcheng.org	beijing jingdong 36
		- jingjing.com	          zhou yongyue
		- jingpinhui.cn         	翟小丽
		- jingpinhui.com	     beijing jingdong 360 du e-commerce ltd.
		- liuqiangdong.com	     liu qiang dong
		- mayshijia.com	         zhang yan
		- minitiao.cn	         北京京东叁佰陆拾度电子商务有限公司
		- minitiao.com	         周 永跃
		- missjia.net	         zhang yan
		- nancyoffice.com	     zhang yan
		- paidaojia.cn	         北京京东叁佰陆拾度电子商务有限公司
		- paipai.cn	             北京京东叁佰陆拾度电子商务有限公司
		- paipai.com	         domain admin
		- paipai.com.cn	         北京京东叁佰陆拾度电子商务有限公司
		- paipai.net.cn	         北京京东叁佰陆拾度电子商务有限公司
		- paipai.org.cn	         北京京东叁佰陆拾度电子商务有限公司
		- paipai.travel	         tencent holdings limited
		- paipai.tv	             zhou yongyue
		- paipaiimg.com      	zhang yan
		- paipaixd.com	        zhang yan
		- paipaixiaodian.cn	    北京京东叁佰陆拾度电子商务有限公司
		- paipaixiaodian.com	zhang yan
		- portpay.cn	        腾讯科技(深圳)有限公司
		- ppxiaodian.cn	        北京京东叁佰陆拾度电子商务有限公司
		- qianxun.com	        周 永跃
		- qq.jx.cn	            腾讯科技(深圳)有限公司
		- qq.sd.cn	            腾讯科技(深圳)有限公司
		- qqgame.cn	            腾讯科技(深圳)有限公司
		- richardnancycapital.com	zhang yan
		- rtx.org.cn	        腾讯科技(深圳)有限公司
		- supesite.org.cn	     腾讯科技(深圳)有限公司
		- tcimage.cn	         腾讯科技(深圳)有限公司
		- tdog.cn	             北京京东叁佰陆拾度电子商务有限公司
		- tencent.org.cn	     腾讯科技(深圳)有限公司
		- tianqiangcapital.cn	 章泽天
		- tianqiangoffice.cn	 章泽天
		- tianqiangoffice.com	 zhang yan
		- trimg.cn	             腾讯科技(深圳)有限公司
		- tunmint.com.cn	      腾讯科技(深圳)有限公司
		- vg.com	             [querying whois.ename.com
		- wanggou.com	         domain admin
		- xianggou.org	         BEIJING JINGDONG 36
		- xn--xhq9m.com	         zhang yan
		- yixun.com	             domain admin
		- zhan1111.com	         zhang yan
		- zhan618.com	         zhang yan

其中27个子域名：(whois查询）
============================================
		www.vip.jd.com
		ip地址：202.106.199.36
		服务信息：会员服务主页

		www.home.jd.com
		ip地址：202.106.199.36
		www.t.jd.com
		ip地址：202.106.199.36
		www.joycenter.jd.com
		ip地址：202.106.199.36
		www.plus.jd.com
		ip地址：202.106.199.36
		www.imzone.jd.com
		ip地址：111.206.227.147
		服务信息：会员登陆界面



		www.paimai.jd.com
		Ip地址：61.50.248.117
		服务信息：京东拍卖页面

		www.myjd.jd.com/www.channel.jd.com
		Ip地址：61.50.248.117
		服务信息：京东主页面

		www.coll.jd.com
		Ip地址：202.106.199.36
		www.safe.jd.com
		Ip地址：61.50.248.117
		www.giftcard.jd.com
		Ip地址：61.50.248.117
		服务信息：访问失败页面

		www.auction.jd.com
		ip地址：202.106.199.36
		服务信息：京东夺宝岛

		www.z.jd.com
		Ip地址：61.50.248.117
		服务信息：京东众筹，京东金融

		www.help.jd.com
		ip地址：61.50.248.117
		服务信息：京东帮助页面（客户服务，快递查询，售后服务等）

		www.union.jd.com
		ip地址：61.50.248.117
		该域名已经无法访问

		www.en.jd.com
		ip地址：202.106.199.36
		服务信息：京东全球购物网站（针对国外，全英文）

		www.tuan.jd.com
		ip地址：60.50.248.117
		服务信息：京东团购页面（电影团购、旅游团购、服装团购等）

		www.chat5.jd.com
		ip地址：60.50.248.117
		服务信息：京东在线客服（用户入口+商家入口）

		www.red.jd.com
		ip地址：202.106.199.36
		服务信息：京东闪购（品牌活动）

		www.pinpaijie.jd.com
		ip地址：111.206.231.1
		服务信息：品牌特卖

		www.book.jd.com
		ip地址：202.106.199.36
		服务信息：图书售卖页面

		www.jrcashier.jd.com
		ip地址：202.106.199.36
		已经无法访问

		www.xuan.jd.com
		Ip地址：202.106.199.36
		服务信息：天天低价（京东促销大全）

		www.coudan.jd.com
		Ip地址：111.206.227.232
		服务信息：一个开发过程中使用的购物车测试页面

		www.mobile.jd.com
		Ip地址：61.50.248.117
		服务信息：京东通信网上营业厅  
		
		
**风险分析**：　多个域名绑定同一网站可以提高网站的可用性，提供更方便和更全面的服务，但是多个域名绑定同一网站也有一些弊端，对于网站优化来说，网站如果有多个域名同时指向的时候对于抓取是很不利的，在进行网站收录时浏览器会认为三个域名中有两个是复制性网站，便会对其做一个判断：网站质量有问题，影响网站信誉！    
**风险级别**：低。    
**后果**：降低浏览器中网站排名，影响信誉度。措施适量减少指向同一ip的域名。    
**措施**：措施适量减少指向同一ip的域名。  


    4个DNS服务器：
    NS1.JDCACHE.COM
    ip地址：111.13.28.10
    
    NS2.JDCACHE.COM
    ip地址：111.206.226.10
    
    NS3.JDCACHE.COM
    ip地址：120.52.149.254
    
    NS4.JDCACHE.COM
    ip地址：106.39.177.32
    
     **风险分析：**每一个服务器都有许多个ip地址，dns服务器的主数据库中存储着很多域名以及ip地址，我们要得到服务器的ip地址很容易。dns服务器存在的风险就是DNS欺骗攻击，也是一种中间人攻击。客户端首先以特定的标识向DNS服务器发送域名查询数据报，在DNS服务器查询之后以相同的ID号给客户端发送域名响应数据报。这时客户端会将收到的DNS响应数据报的ID和自己发送的查询数据报ID相比较，如果匹配则表明接收到的正是自己等待的数据报，如果不匹配则丢弃之。假如攻击者能够伪装DNS服务器提前向客户端发送响应数据报，那么客户端的DNS缓存里域名所对应的IP就是攻击者自定义的IP了，当一台主机访问京东的服务器时，攻击者利用一些工具，例如ettercap，将目标主机所发送的数据包转移到攻击者的主机，并且攻击者任意修改后再发送给服务器，这样，攻击者就会获取到用户的机密信息，攻击者假冒服务器端后也可以发送攻击者想要目标主机访问的任何内容，比如一些不安全网站。另外攻击者也可以向服务器端发送大量的数据包，导致域名无法解析。    
**风险等级：**高。      
**后果：**用户信息泄露，网站无法访问。  
**措施：**服务器端使用SSH加密协议，对数据流加密。进行ip和MAC地址的绑定，预防arp欺骗攻击，因为arp欺骗是dns欺骗的开端。

漏洞：
-------------------------------------------------


**漏洞风险分析：**xss漏洞可分为两种，存储型和触发型，根据我们的漏洞信息收集可以得出一个结论，京东两种都占全了，而且形式多种多样。触发型的有，语序任意文件上传，图片上传，图片过滤不严，这些都给攻击者营造了破坏网站和窃取信息的环境，攻击者可通过在文件或者图片中隐藏恶意代码，当用户点击或查看时触发攻击，使其跳转至恶意网站或者跳出一个登陆页面以获取用户信息，只要会写js代码，那么xss可以用在任何网站任何地方。存储型xss攻击会把攻击者的数据存储在服务器端，攻击行为将伴随着攻击数据一直存在，当用户首次登入网站时，服务器为该用户创建一个 session ID，同时向浏览器传送一个 cookie，cookie保存会话连接中用到的数据，session ID作为会话标识，浏览器后续的请求均基于该session ID。攻击者先以普通用户的身份登陆，然后向服务器发送一条带有特殊js代码的消息，这条特殊代码将存储在服务器的数据库中，一旦管理员登陆，攻击者就可以获得管理员的 session ID,有了这个攻击者就可以在数据库中为所欲为。因为攻击者写的代码一直都存在于数据库中，如果程序员没有发现，那么将一直成为威胁。  
**风险级别：**高。    
**后果：**获取用户信息，链接恶意网站，破坏网站，攻击者进入数据库。  
**措施：**通过定义白名单的形式，例如只允许<p> <div> <a>标签，只允许href class style属性。然后对每一个可能造成XSS的属性进行特定的过滤。
    

 股权结构：
---------------------------------------------------
![](http://i.imgur.com/XiiEweL.png)

京东管理人员：
--------------------------------------------------
![](http://i.imgur.com/vv9e0K8.jpg)

京东五个主要部门：

1、营销部门

2、运营部门（运营、仓管、配送、客服）

3、信息部门

4、战略部门（人事、行政、法务、公关、基建、战略）

5、财务部门       

CEO（首席执行官）

CMO（首席营销官）  

COO（首席运营官Operating）

CTO（首席测试官Testing）

CSO（首席战略官Strategy/Strategic）

CFO（首席财务官）

