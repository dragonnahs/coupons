<template name="redflower-showTips">
	<view>
		<view class="tipsWrap" v-if="showTips">
			<view class="arrow"></view>
			<view class="tipsContent">
				<text>点击「添加到我的小程序」，下次使用更便捷</text>
				<text class="closeIcon" @tap="closeTips()">X</text>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name: "showTips",
		data() {
			return {
				isFirst: true, //是否首次
				showTips: false, //是否展示
			};
		},

		onReady() {
			const _that = this;
			//获取本地缓存
			let cache = uni.getStorageSync('isFirst');
			if (cache) {
				_that.showTips = false;
			} else {
				console.log(_that.showTips)
				_that.showTips = true;
				uni.setStorage({
					key: 'isFirst',
					data: true
				})
				setTimeout(() => {
					_that.showTips = false;
				}, 60000); //5s后消失
			}
		},

		methods: {
			//手动关闭
			closeTips() {
				const _that = this;
				_that.showTips = false;
				uni.setStorage({
					key: 'isFirst',
					data: true
				})
			}
		}


	}
</script>

<style>
	.tipsWrap {
		position: fixed;
		top: 0;
		/* 距离顶部高度，部分自定义标题栏会覆盖提示栏 */
		right: 0;
		z-index: 99999;
		display: flex;
		justify-content: flex-end;
		align-items: flex-end;
		flex-direction: column;
		width: 600rpx;
		animation: rotate .9s linear infinite;
	}

	/* 弹跳动画 */
	@keyframes rotate {
		0% {
			transform: translateY(0);
		}

		25% {
			transform: translateY(2rpx);
		}

		50% {
			transform: translateY(5rpx) scale(1.01, 0.99);

		}

		75% {
			ransform: translateY(2rpx);
		}

		100% {
			transform: translateY(0);
		}
	}

	.arrow {
		width: 0;
		height: 0;
		margin-right: 120rpx;
		border-width: 10rpx;
		border-style: solid;
		border-color: transparent transparent #007AFF transparent;
		/* 箭头颜色 */
	}

	.tipsContent {
		background-color: #007AFF;
		/* 背景颜色 */
		box-shadow: 0 10rpx 20rpx -10rpx #007AFF;
		/* 阴影颜色 */
		border-radius: 8rpx;
		display: flex;
		align-items: center;
		justify-content: center;
		height: 56rpx;
		padding: 0 10rpx 0 15rpx;
		margin-right: 40rpx;
	}

	.tipsContent>text {
		color: #FFFFFF;
		font-size: 24rpx;
	}

	.closeIcon {
		font-size: 24rpx !important;
		margin-left: 10rpx;
		background: #FFFFFF;
		border-radius: 50%;
		width: 34rpx;
		height: 34rpx;
		line-height: 34rpx;
		text-align: center;
		box-sizing: border-box;
		color: #007AFF !important;
	}
</style>