<template>
	<div class="home-page">
		<v-header></v-header>
		<ul class="nav">
			<router-link to="/ClassifiedList">
				<li v-for="item in arrList">
					<img :src="item.imgUrl" alt="" />
					<span>{{item.name}}</span>
				</li>	
			</router-link>
		</ul>
		<v-course :CourseList="arrayCourse"></v-course>
		<v-footer></v-footer>
	</div>
</template>
<style scoped>
.nav{
	height: 100px;
	padding-top: 44px;
	background: #F3F5F7;
	overflow-x: scroll;
	white-space: nowrap;
}
.nav li{
	width: 88px;
	display: inline-block;
	text-align: center;
	font-size: 14px;
}
.nav li img{
	width: 32px;
	display: block;
	margin: 20px auto 12px;
}
</style>
<script>
	import Header from "@/components/header/";
	import ListCourse from "@/components/list/";
	import Footer from "@/components/footer/";

	import webImg from "@/assets/前端开发@2x.png";
	import webService from "@/assets/后端开发@2x.png";
	import webMobile from "@/assets/移动开发@2x.png";
	import webData from "@/assets/数据库@2x.png";
	import webComputing from "@/assets/云计算&大数据@2x.png";


	import courseSed from "@/assets/course1.jpg";
	import courseJava from "@/assets/course2.jpg";
	import courseStars from "@/assets/course3.jpg";
	import courseAwk from "@/assets/course4.jpg";
	import coursePHP from "@/assets/course5.jpg";

	export default{
		data(){
			return{
				arrList:[],
				arrayCourse:[],
			};
		},
		mounted(){
			this.arrList = [{
				imgUrl : webImg,
				name:'前端开发'
			},{
				imgUrl : webService,
				name:'后端开发'
			},{
				imgUrl : webMobile,
				name:'移动开发'
			},{
				imgUrl : webData,
				name:'数据库'
			},{
				imgUrl : webComputing,
				name:'云计算&大数据'
			}];

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
			'v-header': Header,
			'v-course':ListCourse,
			'v-footer':Footer
		}
	};
</script>