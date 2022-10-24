<template>
	<view>
		<u-navbar back-text="返回" title="预定指南"></u-navbar>
		<view class="top"><img src="https://s1.ax1x.com/2022/10/22/xcTi6S.jpg" alt="" class="topimg" /></view>
		<view class="wenben">
			<view class="yuding">预订方式</view>
			<img src="https://s1.ax1x.com/2022/10/24/x2Nf3V.png" style="width: 100%; height: 250rpx;">
			<view style="width: 95%;margin: 0 auto;margin-top: -10%;">
				<template>	<!--内容 -->
					<view class="u-content"><u-parse :html="content" :tag-style="style"></u-parse></view>
				</template>
			</view>
		</view>
		<u-gap height="15" bg-color="#F4F4F4"></u-gap>
		
		<view class="bottle">
			<view class="weizhi">
				<text style="color: azure;">随 时 为 您 服 务</text>
				<view class="lxkf" @click="kefu">联系客服</view>
			</view>
		</view>
		<u-gap height="20" bg-color="#F4F4F4"></u-gap>
	</view>
</template>

<script>
export default {
	data() {
		return {
			content: `
				
					<p>在线支付</p>
				请致电全国客服热线000-0000000或各网点抢修电话。
					<br />			
					1.单击主页右上角的“在线支付”按钮，选择需要预付款的订单进行支付操作；<br />	
					2.单击“支付”按钮后，在跳转后的支付页面中选择任一支付方式、完成预付租车款；<br />	
					3.返回“订单管理”页面，确认订单状态为“已预付”<br />	<br />	
					<p>修改订单</p>
					<text>您可以通过以下方式修改订单：</text>
					<br />
					A. 客服热线00000或登录我的帐户进行修改 <br />
					B. 在线订单修改（网站预订订单） <br />
					1). 登录“我的帐户”；<br />
					2). 进入“我的订单”，选择需要修改的订单进行操作；<br />
					3). 单击“修改”按钮，页面跳转订单修改页面后进行修改即可；<br /><br />
					<text class="yangshi">注意事项：</text>
					<br />
					1）国定节假日订单修改时间以适时官网信息为准<br />
					2）订单的计算价格是根据系统进行显示，任何的订单信息更改都可能会影响订单的终价格<br />

				`,
			style: {
				// 字符串的形式
				text: 'color: #000;font-size:30rpx;font-weight:bold',
				p: 'color: #0076FE;font-size:40rpx',
				span: 'font-size: 20rpx'
			}
		};
	},
	methods: {
		kefu(){
			uni.makePhoneCall({
				phoneNumber: '15216419756' //仅为示例
			});
		}
	}
};
</script>

<style>
.topimg {
	width: 100%;
	height: 400rpx;
}
.top {
	height: 420rpx;
	background: #f4f4f4;
}
.wenben {
	margin-top: 20rpx;
	margin-left: 10rpx;
}
.bt {
	height: 30rpx;
	line-height: 30rpx;
	color: #3982f7;
	font-size: 30rpx;
	margin-top: 15rpx;
}
.yuding{
	margin-left: 5%;
	color: #0076FE;
	font-size:40rpx;
	margin-bottom: 5%;
}
.yangshi {
	margin-bottom: 10rpx;
}.bottle{
	width: 100%;
	height: 250rpx;
	background-image: url("https://s1.ax1x.com/2022/10/22/xcXKUg.jpg");
	background-size: 100% auto;
}
.weizhi{
	padding-top: 7%;
	line-height: 70rpx;
	padding-left: 7%;
}
.lxkf{
	width: 200rpx;
	height: 70rpx;
	text-align: center;
	line-height: 70rpx;
	background: #fff;
	color: #F89101;
}
	.u-content {
		margin-top: 100rpx;
		color: $u-content-color;
		font-size: 29rpx;
		line-height:2;
		
	}
</style>
