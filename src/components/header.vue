<template>
	<div class="c-header">
		<ul class="header-ul">
			<li>推荐</li>
			<li class="active">课程</li>
			<li>实战</li>
			<li>职业路线</li>
			<li class="header-search"><img src="../../src/assets/search.png" /></li>
			<li class="header-history"><img src="../../src/assets/history.png" /></li>
		</ul>
	</div>
</template>
<style scoped>
.c-header{
	position: fixed;
	z-index: 3;
	width: 375px;
	top: 0;
	background: #FFFFFF;
	box-shadow: 0 2px 4px 0 rgba(0,0,0,0.10);
}
.header-ul{
	font-size: 0;
}
.header-ul li{
	display: inline-block;
	padding-left: 20px;
	font-size: 16px;
	color: #71777D;
	line-height: 44px;
}
.header-ul img{
	width: 18px;
}
.header-ul .header-search{
	padding-left: 60px;
}
.header-history{

}
.header-ul .active{
	color: #2B333B;
	text-decoration: overline red;
}
</style>