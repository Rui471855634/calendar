#Calender 日历控件使用说明

## 初始化:
```
 var uiCalender = calender({
	id: "#cl_panel",
	date: date, //设置今天的日期 Date对象
	type: "month"||"dw"||"w", //month月日历 dw双周日历 w周历日  默认为month
	pageHandler: true, //翻页按钮 默认为true
	lunarCalender：true, //是否加载农历日期，默认为true
	//pickerdateSelector: true, //滚动日期选择器 默认为false
	style: "miui", //风格 normal:普通日历风格  miui:小米日历风格  默认为normal
	pageNum: 12, //一次性创建的日历数量，建议使用双数,默认为3
	direction: "x", //日历滑动方向 默认为x  x|y
	dayHeight: "40", //日期模块的高度，建议大于等于40，若zoom为true 则大于等于0.6，默认为屏幕宽度除以7
	zoom: false, // 保持比例缩放 默认false
	onMove: function(){ //作用滑动的回调
	
	},
	onLoad: function(){ //加载完成后的回调
	
	},
	callback: function(){ //点击后的回调
	
	}
});
```

## 方法:

uiCalender.getDate();
uiCalender.setDate(date); //date为日期对象
uiCalender.setType(type, date); //type:month月日历 dw双周日历 w周历日  默认为month;date为日期对象，选填
uiCalender.setStatus(status, date); //设定日期下方圆点，表示状态。 status 0:未完成  1:已完成  -1:无标记; date传被标记日期对象
uiCalender.hide()
uiCalender.show()
uiCalender.getFirstDay(index) //获取日历显示出来的的第一天。 index：-1：上个月 0：本月 1：下个月
uiCalender.getLastDay(index) //获取日历显示出来的的最后一天。 index：-1：上个月 0：本月 1：下个月