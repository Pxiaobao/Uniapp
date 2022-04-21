<template>
	<view>
			<view class="fs-30">
				欢迎使用uniapp开发
			</view>
			<view class="fs-24"> 
				欢迎使用uniapp开发
			</view>
			<view class="fs-26">
				欢迎使用uniapp开发
			</view>
			<view class="title">
					<text class="iconfont icon-vip-fill"></text>
			</view>
			<text>{{msg}}</text>
			<input v-model="msg"></input>
			<!-- 动态使用属性(v-bind可省略)的三种方式 -->
			<view class="box" v-bind:class="isActive?'active':''">
			</view>
			<view v-bind:class="['box',isActive?'active':'']">
			</view>
			<view v-bind:class="['box',{'active':isActive}]">
			</view>
			<!-- 动态使用src属性-->
			<image v-bind:src=imags[loginState] mode=""></image>
			<button v-on:tap="changeimg" type="primary">控制图片变化</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				msg:'这是数据',
				isActive:false,
				loginState:0,
				imags:[
					'../../static/img/banner.jpg',
					'../../static/img/french.jpg'
				]
				
			};
		},
		methods:{
			changeimg:function(){
				this.loginState = this.loginState===0?1:0
			}
		}
	}
</script>

<style lang="scss">
.title{
	color: #007AFF;
}
.icon-vip-fill{
	font-size: 100rpx;
}
.box{
	height: 200rpx;
	width: 200rpx;
	border: 1px solid red;
}
.box.active{
	background-color: #007AFF;
}
</style>
