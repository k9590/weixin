<template>
	<view>
		<!-- <image class="logo" src="/static/logo.png"></image> -->
		<view class="Top"></view>
		<view class="content">
			<!-- 搜索框 -->
			<view class="seec" @click="THBN">
				<u-icon size="30" name="search"></u-icon>
				<text>搜索品牌、车型</text>
			</view>
			<br />
			<!-- 图标 -->
			<view class="Tabulation"><img src="https://s1.ax1x.com/2022/10/24/x2NUht.png" style="width: 100%; height: 230rpx;" /></view>
			<view class="swiper_box"><u-swiper :list="list" :mode="rect" height="350"></u-swiper></view>
		</view>
		<view class="hullbottom">
			<u-divider>车型排行</u-divider>
			<view style="margin-bottom: 5%; margin-top: 5%;">
				<scroll-view class="scroll-view_H" scroll-x="true" @scroll="scroll" scroll-left="120">
					<view id="demo1" class="scroll-view-item_H uni-bg-red">
						<view class="xhss">
							<img src="https://s1.ax1x.com/2022/10/22/xcoIF1.jpg" />
							<br />
							别克GL8
							<br />
							￥140/天起
						</view>
					</view>
					<view id="demo2" class="scroll-view-item_H uni-bg-green">
						<view class="xhss">
							<img src="https://s1.ax1x.com/2022/10/22/xcohw9.jpg" />
							<br />
							宾利天越
							<br />
							￥250/天起
						</view>
					</view>
					<view id="demo3" class="scroll-view-item_H uni-bg-blue">
						<view class="xhss">
							<img src="https://s1.ax1x.com/2022/10/22/xco1II.jpg" />
							<br />
							广汽传祺
							<br />
							￥120/天起
						</view>
					</view>
				</scroll-view>
			</view>
			<br />
			<!-- 	<view class="uni-common-pb">
				
			</view> -->
			<view style="width: 95%; margin: 0 auto;  margin-bottom: 5%; "><u-section title="热门新闻" sub-title="查看全部"></u-section></view>
			<template>
				<u-card>
					<view class="" slot="body">
						<view class="u-body-item u-flex u-border-bottom u-col-between u-p-t-0">
							<view class="u-body-item-title u-line-2">买车，租车，打车，哪种出行方案对你性价比较高</view>
							<image src="https://365632.s81i.faiusr.com/2/105/AFEIwKgWEAIYACD346jdBSjGrMb8AjCgATh4QGk.jpg" mode="aspectFill"></image>
						</view>
						<view class="u-body-item u-flex u-row-between u-p-b-0">
							<view class="u-body-item-title u-line-2">汽车租赁模式分析及汽车租赁风控深度解读</view>
							<image src="https://365632.s81i.faiusr.com/2/105/AFEIwKgWEAIYACD546jdBSj00dDQBTCgATh4QGk.jpg" mode="aspectFill"></image>
						</view>
						<view class="u-body-item u-flex u-row-between u-p-b-0">
							<view class="u-body-item-title u-line-2">租车的朋友们在租期内应该注意的事项</view>
							<image src="https://365632.s81i.faiusr.com/2/105/AFEIwKgWEAIYACD746jdBSiCwaqWBjCgATh4QGk.jpg" mode="aspectFill"></image>
						</view>
					</view>
				</u-card>
			</template>
			<u-divider>开启自驾之旅</u-divider>
			<view style="margin-bottom: 5%; margin-top: 5%;"><view style="height: 440rpx;">
				<scroll-view class="scroll-view_H" scroll-x="true" @scroll="scroll" scroll-left="120">
					<view id="demo1" class="scroll-view-item_H uni-bg-red">
						<view class="xhss">
							<img src="https://s1.ax1x.com/2022/10/24/x23f1g.jpg"><br>
							广州
						</view>
					</view>
					<view id="demo2" class="scroll-view-item_H uni-bg-green">
						<view class="xhss">
							<img src="https://s1.ax1x.com/2022/10/24/x23W9S.jpg"><br>
							上海
						</view>
					</view>
					<view id="demo3" class="scroll-view-item_H uni-bg-blue">
						<view class="xhss">
							<img src="https://s1.ax1x.com/2022/10/24/x23Ins.jpg"><br>
							深圳
						</view>
					</view>
					<view id="demo4" class="scroll-view-item_H uni-bg-blue">
						<view class="xhss">
							<img src="https://s1.ax1x.com/2022/10/24/x28Q4f.jpg"><br>
							北京
						</view>
					</view>
				</scroll-view>
			</view></view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			scrollTop: 0,
			old: {
				scrollTop: 0
			},
			list: [
				{
					image: 'https://s1.ax1x.com/2022/10/22/xco4oR.jpg'
				},
				{
					image: 'https://s1.ax1x.com/2022/10/22/xcooJx.jpg'
				}
			]
		};
	},
	onLoad() {},
	methods: {
		THBN() {
			console.log(345);
			uni.navigateTo({
				url: '../search/search'
			});
		},
		upper: function(e) {
			console.log(e);
		},
		lower: function(e) {
			console.log(e);
		},
		scroll: function(e) {
			console.log(e);
			this.old.scrollTop = e.detail.scrollTop;
		},
		goTop: function(e) {
			// 解决view层不同步的问题
			this.scrollTop = this.old.scrollTop;
			this.$nextTick(function() {
				this.scrollTop = 0;
			});
			uni.showToast({
				icon: 'none',
				title: '纵向滚动 scrollTop 值已被修改为 0'
			});
		}
	}
};
</script>
<!-- 上半 -->
<style>
/* 头部 */
.Top {
	width: 100%;
	height: 150rpx;
	background: #f4f4f4;
}
/* 搜索框  表格  轮播 */
.content {
	width: 100%;
	height: 360rpx;
	background: #f4f4f4;
	/* border-bottom-left-radius: 80rpx; */
	/* border-bottom-right-radius: 80rpx; */
	text-align: center;
}
/* 搜索框 */
.seec {
	display: flex;
	align-items: center;
	padding: 0 20rpx;
	width: 90%;
	height: 60rpx;
	color: #919191;
	font-size: 15;
	background-color: #fff;
	margin: 0 auto;
	border-radius: 50rpx;
}
/* 表格 */
.Tabulation {
	margin: 15rpx 0;
}
.tabulation {
	margin: 0 auto;
	width: 90%;
	bg-color: #000;
}
.u-tr {
	text-align: center;
}
.u-tr img {
	width: 60rpx;
	height: 60rpx;
}
.Tabulation {
	display: flex;
} /* 轮播 */
.swiper_box {
	width: 100%;
	height: 350rpx;
	border: #0000ff;
	margin: 0 auto;
	margin-top: 15rpx;
	box-shadow: 0 0 15rpx #a9a5a0;
	/* border-radius: 20rpx; */
	overflow: hidden;
}
</style>
<!-- 下半 -->
<style>
.hullbottom {
	margin-top: 400rpx;
}
/* 标题 */
.Caption {
	text-align: center;
	margin: 50% 0;
}
/* 横向滚动 */
.scroll-view_H {
	white-space: nowrap;
	width: 100%;
	display: flex;
	flex-wrap: nowrap;
}
.scroll-view-item_H {
	display: inline-block;
	width: 40%;
	height: 300rpx;
	line-height: 40rpx;
	text-align: center;
	/* font-size: 36rpx; */
}

.u-card-wrap {
	background-color: $u-bg-color;
	padding: 1px;
}

.u-body-item {
	font-size: 32rpx;
	color: #333;
	padding: 20rpx 10rpx;
}

.u-body-item image {
	width: 120rpx;
	flex: 0 0 120rpx;
	height: 120rpx;
	border-radius: 8rpx;
	margin-left: 12rpx;
}
.xhss img {
	width: 80%;
	height: 200rpx;
}
</style>
