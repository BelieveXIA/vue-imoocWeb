<template>
	<ul class="footer">
		<li class="active" ><img src="../assets/首页-选中@2x.png" /><span>首页</span></li>
		<li><img src="../assets/发现@2x.png" /><span>发现</span></li>
		<li><img src="../assets/下载@2x.png" /><span>下载</span></li>
		<li><img src="../assets/我的@2x.png" /><span>我的</span></li>
	</ul>
</template>
<style>
.footer{
	width: 375px;
	height: 49px;
	position: fixed;
	bottom: 0;
	opacity: 0.9;
	background: #FFFFFF;
	border: 1px solid #ddd;
	z-index: 3;
	display: flex;
}
.footer li{
	display: flex;
	height: 50px;
	flex: 1;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	font-size: 10px;
}
.footer li img{
	width: 24px;
}
.footer .active{
	color: #F01414;
}
</style>
