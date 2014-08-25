#timespanjs
##简介
实现日期差值的人性化显示的javascript库。比如，可以显示成：2年2个月2小时4分钟23秒。同时支持国际化,可扩展。已经支持的语言：
+ 中文简体（zh-cn）
+ 中文繁体（zh-tw）
+ 英文（en）
采用[MIT 许可协议](https://github.com/houyhea/timespanjs/blob/master/LICENSE)。
###如何使用
1. 创建Timespan对象。可以通过构造函数中传递时间差值创建，也可以通过传递两个Date对象实例创建。
2. 调用humanize实例方法，获取人性化显示字符串。
比如：
```js
var msvalue = 30+1000*25+1000*60*4+1000*60*60*3;//该值表示为：3小时4分钟25秒30毫秒
var ts = new Timespan(msvalue, 'ms');
console.log(ts.humanize());//输出为：3小时4分钟25秒30毫秒

//通过fromDates方法构造
var dt=new Date("2014-7-1");
var dt1=new Date("2014-8-1 10:12:15:234");
var ts=Timespan.fromDates(dt,dt1);
console.log(ts.humanize());//输出：1个月1天10小时12分钟15秒，234毫秒未输出，因为baseUnit参数默认是:'s'
```
##API说明
见[api说明](https://github.com/houyhea/timespanjs/blob/master/doc/api.md)。
##测试用例
见[https://github.com/houyhea/timespanjs/blob/master/test/testTimespan.html](https://github.com/houyhea/timespanjs/blob/master/test/testTimespan.html)。请获取并运行即可。
##帮助
支付宝赞助（houyhea）：  
![赞助](https://raw.githubusercontent.com/houyhea/lab/master/alipayqrcode.png)