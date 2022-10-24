<template>
	<view>
		<u-navbar back-text="返回" title="带驾服务"></u-navbar>
		<view class="top"><img src="https://s1.ax1x.com/2022/10/22/xcTVTs.jpg" alt="" class="topimg" /></view>
		<view style="width: 95%; margin: 0 auto; margin-bottom: 5%; margin-top: 5%;"><u-section title="服务项目" sub-title="查看全部" @click="View"></u-section></view>
		<view style="margin-left: 30rpx; margin-bottom: 5%;"><img src="https://s1.ax1x.com/2022/10/22/xcTCSf.jpg" alt="" class="fuwuleixing" @click="tiaozhuan" /></view>
		<text style="margin-left: 30rpx; margin-bottom: 5%;">服务项目</text>
		<u-divider>服务预约</u-divider>
		<!-- 表单 -->
		<view style="width: 95%; margin: 0 auto; margin-bottom: 5%;">
			<template>
				<u-field v-model="mobile" label="姓名" placeholder="请填写姓名" required></u-field>
				<u-field v-model="code" label="手机号" placeholder="请填写手机号" required></u-field>
				<u-calendar v-model="showe" :mode="mode"></u-calendar>
				<view style="display: flex;margin: 35rpx auto;">
					<view style="margin-left: 5%;">日期</view>
					<view class="riqi" @click="showe = true">请选择日期</view>
				</view>

				<view style="margin-top: 5%;">
					<u-field @click="showAction" v-model="sex" :disabled="true" label="出行服务" placeholder="请选择需要的服务" right-icon="arrow-down-fill"></u-field>
					<u-action-sheet @click="clickItem" :list="sexList" v-model="show"></u-action-sheet>
				</view>
			</template>
			<br>留言<br><br>
			<u-input v-model="value" :type="type" :border="border" :height="height" :auto-height="autoHeight" />
			<br>
			<u-button :ripple="true" ripple-bg-color="#3979F7">马上预约</u-button>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			value: '',
			type: 'textarea',
			border: true,
			height: 100,
			autoHeight: false,
			show: false,
			mode: 'date',
			mobile: '',
			code: '',
			sex: '',
			sexList: [
				{
					text: '机场接送'
				},
				{
					text: '市内点到点接送'
				},
				{
					text: '城际点到点接送'
				},
				{
					text: '全天/半天代驾'
				}
			],
			showe: false
		};
	},
	methods: {
		// 查看全部
		View() {
			//在起始页面跳转到test.vue页面并传递参数
			uni.navigateTo({
				url: '../View/View'
			});
		},
		tiaozhuan() {
			//在起始页面跳转到test.vue页面并传递参数
			uni.navigateTo({
				url: '../Service/Examine/Examine'
			});
		},
		showAction() {
			this.show = true;
		},
		clickItem(index) {
			this.sex = this.sexList[index].text;
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
.fuwuleixing {
	width: 95%;
	height: 400rpx;
	margin: 0 auto;
}
.riqi {
	width: 70%;
	margin-left: 5%;
	height: 60rpx;
	color: #d5d5d5;
	/* background: #000; */
}
</style>
