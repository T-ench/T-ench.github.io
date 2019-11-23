---
layout:     post   				    # 使用的布局（不需要改）
title:      My First Blog 				# 标题 
subtitle:   Hello World, Hello Blog #副标题
date:       2019-11-18 				# 时间
author:     Tench 						# 作者
header-img: img/post-bg-2015.jpg 	#这篇文章标题背景图片
catalog: true 						# 是否归档
tags:								#标签
    - 生活
---

## Hey
>这是我的第一篇博客。

### 这是一个秒表计时器网页代码
```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style type="text/css">		
		#div1{
			width: 300px;
			height: 400px ;
			background-color: gray;
			margin: 100px auto;
			text-align: center ;
			}
		#count{			I
			width: 200px;
			height: 150px ;
			line-height: 150px;
			margin:	auto;
			font-size: 40px
			}
		#div1 input
			{
			width: 150px; 
			height: 40px; 
			background-color:yellow; 
			font-size: 25px;
			margin-top: 20px}
		</style>
		<script type="text/javascript">
			function $(id){
				return document . getElementById( id);
			}
			
			window.onload = function( ){
				//点击开始开始计数
				var count = 0; //开始计数以后，累加的总秒数
				var timer = null;
				$("start").onclick = function(){
					timer = setInterval(function(){
						count++;
							//需要改变 页面上时分秒的值。
						$("id_S").innerHTML = showNum(count%60);
						$("id_M").innerHTML = showNum(parseInt(count/60)% 60);
						$("id_H").innerHTML = showNum(parseInt(count/3600));

					},100);
				}
				
				$("pause").onclick = function(){
					//取消定时器
					clearInterval(timer);
				}
				
				$("stop").onclick = function(){
					//取消定时器 
					clearInterval(timer);	
					count = 0;
					$("id_S").innerHTML = "00";
					$("id_M").innerHTML = "00";
					$("id_H").innerHTML = "00";			
				}
			}
			
			function showNum(num){
				if(num < 10){
					return "0"+ num;
				}else{
					return num;
				}
			}
		</script>
	</head>
	<body>
	
		<div id="div1">
			<div id="count">
				<span id = "id_H">00</span> :
				<span id = "id_M">00</span> : 
				<span id = "id_S">00</span>
			</div>
		
		<input id = "start" type = "button"value = "开始" /> 
		<input id = "pause" type = "button" value = "暂停" />
		<input id = "stop"  type = "button" value = "停止" />
		</div>
	</body>
</html>
```
### 从小到大js冒泡排序
```
for（var i=0; i<arr.length; i++){
	for(var j=0; j<arr.length-i-1; j++){
		if(arr[j]>arr[j+1]){
			var tmp = arr[j+1];
			arr[j+1]=arr[j];
			arr[j]=tmp;
		}
	}
}
```

### 从小到大选择排序
```
for（var i=0; i<arr.length-1; i++){
    for(var j=i+1; j<arr.length; j++){
        if(arr[i]>arr[j]){
            var tmp = arr[i];
            arr[i]=arr[j];
            arr[j]=tmp;
        }
    }        
}
```


