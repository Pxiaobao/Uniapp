<template>
	<view>
		<view v-for="(item,index) in stu" :key="index">
			序号：{{index}}, 姓名：{{item.name}}, 分数：{{item.age}}
		</view>
		<view v-for="(item,index) in stu" :key="index">
			序号：{{index}}, 姓名：{{item.name}}, 分数：{{item.age}}
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				stu:[
						{name:'张三',age:20},
						{name:'李四',age:30},
						{name:'王五',age:10},
				]
			};
		}
	}
</script>

<style lang="scss">

</style>
