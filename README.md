	#完整轮播图
	##第一遍：总结
	1.逻辑要清晰，最好写代码之前，有思路
	2.操作的什么dom一定要清晰 比如 ol 和 ul 的区别
	3.元素的操作要熟练 ： 比如： removeAttribute（class) 
	4.细心注意细节
	
	//写代码最好，从逻辑开始
	//先总结出东西怎么写
	
	###完成轮播图注意：
	1.根据图片个数，生成<ol>
	2.right里得无缝连接
	3.left里面的无缝连接
	4.通过setinterval来控制自动轮播
	/5.通过animate来生成动画

	###具体
	/*
	Tag
	1.get图片个数
	2.通过for循环生成li
	2.为li，innerHTML设置内容
	3.设置index，内容为li
	
	Tag:onmouseover
	1.通过for循环设置ol,li:className为current
	2.其他为空
	3.通过下标数控制移动,整个图片元素
	设置全局pic为，后面做好准备
	pic等于index的下标；
	4.animte(ul,- pic*width): 整个ul在往左所以是负数
	
	>:onmouseover 
	1.外部设置移动函数的间隙调用
	2.正常调用
	3.标签display：block
	<:onmouseout
	1.display：none
	2.清楚计时器
	
	
	left:>:click：调用移动函数
	移动函数：无缝连接，
	1.当pic值为5的时候
	pic = 0； 
	animte()到0的位置
	2.!!!注意：此时无法达到无缝效果，需要克隆节点
	cloneNode(ture)
	
	3.p++
	正常animte
	
	4.ol跟随变化
	当pic=5
	ol的0位current
	其他为"" 
	
	其他情况正常处理：
	pic为current，其他为空
	
	right:click
	
	right:>:click：调用移动函数
	1.当pic= 0
	pic = 5
	移动到5的位置
	
	2.正常
	pic--
	animte
	
	2.ol跟随变化
	1.清楚所有class
	2.设置pic为current