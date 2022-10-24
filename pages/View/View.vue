<template>
	<view>
		<u-navbar back-text="返回" title="服务项目"></u-navbar>
		<view class="Top"></view>
		
		<view class="content">
			<img src="https://s1.ax1x.com/2022/10/23/xgcVqx.jpg" class="Img" @click="tiaozhuan">
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			tiaozhuan(){
				uni.navigateTo({
					url: '../Service/Examine/Examine'
				});
			}
		}
	}
</script>

<style>
/* 头部 */
.Top {
	width: 100%;
	height: 50rpx;
	background: #f4f4f4;
}
.content {
	width: 100%;
	height: 1120rpx;
	background: #f4f4f4;
	/* border-bottom-left-radius: 80rpx; */
	/* border-bottom-right-radius: 80rpx; */
	text-align: center;
}
.Img{
	width: 100%;
	height: 400rpx;
}

</style>
