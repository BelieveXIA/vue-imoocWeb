<template>
	<div class="classified-page">
		<div class="classified-header">
			<ul class="classified-title">
				<li><router-link to="/"><img src="../assets/back@2x.png" alt="" class="back" /></router-link></li>
				<li><h1>前端开发</h1></li>
				<li><img src="../assets/search.png" alt="" /></li>
			</ul>
			<ul class="classified-nav">
				<li v-for="item in classList">{{item}}</li>
			</ul>
			<ul class="classified-select">
				<li><span>全部</span><img src="../assets/箭头@2x.png" alt="" /></li>
				<li><span>最新</span><img src="../assets/箭头@2x.png" alt="" /></li>
				<li><span>仅显示未学</span><img src="../assets/滑块@2x.png" alt="" /></li>
			</ul>			
		</div>
		<v-course :CourseList="arrayCourse" class="list"></v-course>
	</div>
</template>
<style>
.classified-header{
	position: fixed;
	top: 0;
	z-index: 3;
	background-color: #fff;
}
.classified-title{
	width: 375px;
	height: 44px;
	font-size: 0;
	position: relative;
	padding: 0 20px;
}
.classified-title li{
	display: inline-block;
	line-height: 44px;
}
.classified-title li h1{
	margin-left: 16px;
	font-size: 16px;
}
.classified-title .back{
	width: 12px;
}
.classified-title li img{
	width: 18px;
}
.classified-title li:nth-last-child(1){
	position: absolute;
	right: 60px;
	top: 13px;
}
.classified-nav{
	width: 375px;
	height: 44px;
	font-size: 0;
	overflow-x: scroll;
	white-space: nowrap;
	padding: 0 20px;
}
.classified-nav li{
	display: inline-block;
	line-height: 44px;
	font-size: 14px;
	margin-right: 24px;
}
.classified-select{
	width: 375px;
	height: 36px;
	font-size: 0;
	position: relative;
	padding: 0 20px;
	border-top: 1px solid #ddd;
	box-shadow: 0 2px 4px 0 rgba(0,0,0,0.10);
}
.classified-select li{
	display: inline-block;
	line-height: 36px;
	font-size: 12px;
	margin-right: 24px;
}
.classified-select li img{
	width: 10px;
}
.classified-select li:nth-last-child(1){
	position: absolute;
	right: 40px;
}
.classified-page .list{
	padding-top: 135px;
}
</style>
<script>

	import ListCourse from "@/components/list/";
	import courseSed from "@/assets/course1.jpg";
	import courseJava from "@/assets/course2.jpg";
	import courseStars from "@/assets/course3.jpg";
	import courseAwk from "@/assets/course4.jpg";
	import coursePHP from "@/assets/course5.jpg";

	export default{
		data(){
			return{
				classList:[],
				arrayCourse:[],
			};
		},
		mounted(){
			this.classList=["全部","HTML/CSS","JavaScript","HTML5","CSS3","Vue"];
			this.arrayCourse = [{
				imgUrl: courseSed,
				alt:'实例妙解Sed和Awk的秘密',
				title: '实例妙解Sed和Awk的秘密',
				lev:'中级',
				stuNum:'357'			
			},{
				imgUrl: courseJava,
				alt:'Java定时任务调度工具详解之Quartz篇',
				title: 'Java定时任务调度工具详解之Quartz篇',
				lev:'中级',
				stuNum:'357'
			},{
				imgUrl: courseStars,
				alt:'星级评分原理与实战',
				title: '星级评分原理与实战',
				lev:'中级',
				stuNum:'357'
			},{
				imgUrl: courseAwk,
				alt:'实例妙解Awk的秘密',
				title: '实例妙解Awk的秘密',
				lev:'中级',
				stuNum:'357'
			},{
				imgUrl: coursePHP,
				alt:'PHP消息队列实践',
				title: 'PHP消息队列实践',
				lev:'中级',
				stuNum:'357'
			},{
				imgUrl: courseJava,
				alt:'Java定时任务调度工具详解之Quartz篇',
				title: 'Java定时任务调度工具详解之Quartz篇',
				lev:'中级',
				stuNum:'357'
			},{
				imgUrl: courseStars,
				alt:'星级评分原理与实战',
				title: '星级评分原理与实战',
				lev:'中级',
				stuNum:'357'
			},{
				imgUrl: courseAwk,
				alt:'实例妙解Awk的秘密',
				title: '实例妙解Awk的秘密',
				lev:'中级',
				stuNum:'357'
			}];
		},
		components:{			
			'v-course':ListCourse,
		}
	};
</script>