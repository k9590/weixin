<template>
	<view>
		<u-navbar back-text="返回" title="客户服务"></u-navbar>
		<view class="top"><img src="https://s1.ax1x.com/2022/10/22/xcTEwj.jpg" alt="" class="topimg" /></view>
		<u-gap height="15" bg-color="#F4F4F4"></u-gap>
		<view class="wenben">
			<view style="width: 95%;margin: 0 auto;">
				<template>
					<view class="u-content"><u-parse :html="content" :tag-style="style"></u-parse></view>
				</template>
			</view>
		</view>
		<u-gap height="15" bg-color="#F4F4F4"></u-gap>
		
		<!-- <u-gap height="15" bg-color="#F4F4F4"></u-gap> -->
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
				
					<p>紧急救援</p>
				请致电全国客服热线000-0000000或各网点抢修电话。
					<br />			
					<text >A. 抢修</text>
					<br />
					1）市区内发生车辆紧急故障，抢修人员将在靠前时间内 提供电话指导，需要提供现场协助的，我们承诺市区范围内2小时到达。
					<br />
				
						2）外省市发生紧急故障，请拨打全国客服热线000-000，我们将为您安排当地指定维修点进行维修。如当地无指定维修点，我们将为您安排当地该品牌4S店进行维修。同时需将维修站开具的维修发票、清单及更
						换的旧件一并带回。
				
					<br />
					<text>B. 替代车</text>
					<br />
					我们会判断是否能现场排除故障，若不能现场排除故障的，在有服务网点的地区，我们将为您更换事故车辆。
					<br />
					<text class="yangshi">C. 车辆维修及替代车费用</text>
					<br />
					1）若车辆属于正常维修范围，维修费用均由我们承担。如果因您操作不当导致车辆损坏，该维修费用需要您自行承担。
					<br />
					2）正常的车辆维修期间，我们将免费提供替代车辆供您使用。如属于人为损坏造成的维修，替代车辆的租金 将由您自行承担。该车辆租金将根据合同约定的费用收取。
					<br /><br />
					<p>事故理赔</p>
					<br />
					拨打全国客服热线00000或拨打服务公司的报案电话。<br />
					1）我们提供事故处理的电话指导服务，必要时我们将提供现场协助服务；<br />
					2）拨打110报警电话，开具事故责任认定书；<br />
					3）配合服务公司完成车辆定损，必要时向服务公司索取 报案号；<br />
					4）指定维修站维修；<br />
					5）垫付维修费用，并索取维修发票和维修清单；<br />
					6）提交进保资料保险公司；<br />
					7）理赔退款。<br />
				`,
			style: {
				// 字符串的形式
				text: 'color: #000;',
				p: 'color: #0076FE;font-size:40rpx',
				span: 'font-size: 20rpx'
			}
		};
	}
	,methods:{
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
	height: 340rpx;
	background: #f4f4f4;
}
.wenben {
	/* margin-top: 10rpx; */
	margin-left: 10rpx;
}
.bt {
	height: 30rpx;
	line-height: 30rpx;
	color: #3982f7;
	font-size: 30rpx;
	margin-top: 15rpx;
}
.yangshi {
	margin-bottom: 10rpx;
}
.bottle {
	width: 100%;
	height: 250rpx;
	background-image: url('https://s1.ax1x.com/2022/10/22/xcXKUg.jpg');
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
