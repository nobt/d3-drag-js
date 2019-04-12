# d3-drag-js
用到插件d3.js: http://d3js.org/d3.v4.min.js
# 功能
1. 节点可以拖动
2. 可以缩放
3. 可以修改当前图片
# 扩展
1. 在TpGraph.min.js提供了点击事件、以及初始化每个节点的位置
```javascript
/**
* 化图片
*/
var imgMap = {
	'0':'img/net.png',
	'1':'img/switch.png',
	'2':'img/modem.png',
	'error-tip':'img/tip.png',
	'link-cut':'img/cut.png'
};
/**
* 配置
*/
var option = {
	container:'#tpContainer',
	data:'js/data.json',
	width:window.innerWidth || document.documentElement.clientWidth,
	height:window.innerHeight || document.documentElement.innerHeight,
	classedfixed: false,//默认节点没有初始化坐标
	clickevent: function(obj, d){
	  //节点单击事件code
	},
	dblclickevent: function(obj, d){
	  //节点双击事件code
	},
	mouseenterevent: function(obj, d){
	  //鼠标移到节点code
	},
	mouseleave: function(obj, d){
	  //鼠标离开节点code
	}	
};
//初始化
TpGraph.init(option, imgMap);
```
2. 在TpGraph.min.js提供getNodesCoordinate()方法获取每个节点的全部数据，也可以获取每个节点指定的数据
获取全部数据
```javascript
TpGraph.getNodesCoordinate()
```
获取指定参数的值，此时只能传数组: 例如获取每个节点的下x,y的坐标
```javascript
TpGraph.getNodesCoordinate(['x','y']);
```	
		
	
	
	
