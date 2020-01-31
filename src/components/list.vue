<template>
	<ul class="list-course">
		<router-link to="/detail">
			<li v-for ="item in CourseList">
				<img :src="item.imgUrl" :alt="item.alt" />
				<h1>{{item.title}}</h1>
				<p>{{item.lev}} · {{item.stuNum}}人在学</p>
			</li>
		</router-link>
	</ul>
</template>
<style>
.list-course{
	padding-top: 24px;
}
.list-course li{
	position: relative;
	width: 335px;
	height: 72px;
	margin : 0 auto 24px;
}
.list-course li img{
	width: 108px;
	border-radius: 5px;
	position: absolute;
	font-size: 13px;
}
.list-course li h1{
	padding-left: 124px;
	font-size: 15px;
	color: #2B333B;
	line-height: 17px;
}
.list-course li p{
	font-size: 12px;
	color: #71777D;

	padding: 8px 0 0 124px;
}
</style>
<script>
	export default{
		props:{
			CourseList:Array
		}
	};
</script>