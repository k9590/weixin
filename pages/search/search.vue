<template>
	
	<view>
		<u-navbar back-text="返回" title="搜索"></u-navbar>
		<view class="Top"></view>
		
		<view class="content">
			<u-search :show-action="true" action-text="搜索" :animation="true" bg-color="#ffffff"></u-search>
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
/* 搜索框 */
.u-search{
	bg-color: #f4f4f4;
	
}
</style>
