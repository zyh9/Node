## Node

### 初识node.js

	NodeJS——后台
	
	JavaScript-前台
		
		后台：
		1.PHP
		2.Java
		3.Python
		...
		
		优势
		1.性能
			nodejs	php		86
			
			有人大致做了测试，node的性能是php的86倍
		
		2.跟前台JS配合方便
		
		3.NodeJS便于前端学习
		
		一些windows小操作：
		
			1.切换盘符	e:
			2.改变目录	cd 目录名
			3.执行程序	node xxx.js

### 创建一个简单的服务器

		nodeJS——服务器
		
		http——协议
		
		request	请求	输入-请求的信息
		response	响应	输出-输出的东西
		
		每个服务器可提供多种服务，可设置多个端口，以区分每个端口对应不同的服务

```javascript
	//引入http系统模块
	const http=require('http');
	//创建一个一个服务器，接收一个回调函数，返回一个server对象
	//每当访问这个服务器的时候，这个回调函数就会执行
	let server=http.createServer(function (req, res){
	  	//console.log('有人来了');
	
	  	res.write("abc");
	  	res.end();
	});
	
	//监听--等着
	//端口--数字
	server.listen(8080);
```
