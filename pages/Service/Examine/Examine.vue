<template>
	<view>
		<u-navbar back-text="返回" title="详细页"></u-navbar>
		<view style="width: 95%; margin: 0 auto;">
			<img src="https://s1.ax1x.com/2022/10/22/xcTCSf.jpg" alt="" />
			<text>机场接送</text>
			<img src="https://s1.ax1x.com/2022/10/22/xcTFOg.jpg" alt="" />
			<text>城际点到点接送</text>
			<img src="https://s1.ax1x.com/2022/10/22/xcTAmQ.jpg" alt="" />
			<text>市内点到点接送</text>
			<img src="https://s1.ax1x.com/2022/10/22/xcTPl8.jpg" alt="" />
			<text>全天半天代驾</text>
			<view style="height: 30rpx;"></view>
		</view>
		<u-gap height="20" bg-color="#F4F4F4" style="margin-top: 5%;"></u-gap>
		<text class="fuwuxiangmu">服务项目</text>
		<u-icon name="share" color="#d6d6d6" size="28" class="fenxiang"></u-icon>
		<u-gap height="20" bg-color="#F4F4F4" style="margin-top: 5%;"></u-gap>
	</view>
</template>

<script>
export default {
	data() {
		return {};
	},
	methods: {}
};
</script>

<style>
img {
	width: 100%;
	height: 400rpx;
	margin-top: 15rpx;
	margin-bottom: 15rpx;
}
.fuwuxiangmu {
	height: 100rpx;
	line-height: 100rpx;
	font-size: 45rpx;
	font-weight: 500;
	margin-left: 15rpx;
}
.fenxiang{
	margin-left: 500rpx;
}
</style>
