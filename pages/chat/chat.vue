<template>
	<view class="chat-box">
		<view class="chat-content">
			<scroll-view scroll-y class="scroll-Y">
				<view class="content" v-for="i in 20" :key="i">
					<view class="chat-content-left uni-flex">
						<view class="chat-icon">
							<image src="/static/default-icon.jpg" mode=""></image>
						</view>
						<view class="chat-info">
							<view class="chat-user">
								askwan
							</view>
							<view class="chat-text" style="background: #fff; color: #333;">
								hello，world都是发发发撒旦发射点发射点发生发射点发手动阀手动阀士大夫撒旦发生的首发式发生发射点发生？
							</view>
						</view>
					</view>
					<view class="chat-content-right uni-flex">
						<view class="chat-info">
							<view class="chat-user" style="text-align: right;">
								askwan
							</view>
							<view class="chat-text">
								hello，world？
							</view>
						</view>
						<view class="chat-icon">
							<image src="/static/default-icon.jpg" mode=""></image>
						</view>
					</view>
				</view>
				
			</scroll-view>
		</view>
		<view class="chat-input uni-padding-wrap uni-flex">
			<input class="uni-input input uni-bold" type="text" value="" />
			<view class="center">
				<button type="primary" size="mini">发送</button>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
	.chat-box{
		$input-height:50px;
		.center{
			display: flex;
			justify-content: center;
			align-items: center;
		}
		.chat-content{
			background: rgba(0,0,0,.1);
			height: calc(100vh - #{$input-height});
			overflow-y: auto;
			.chat-info{
				// border: 1upx solid red;
				padding: 8rpx;
			}
			.chat-icon{
				width: 60rpx;
				height: 60rpx;
				background-color: rgba(0,0,0,.2);
				border-radius: 50%;
				flex-shrink: 0;
				overflow:hidden;
				image{
					width: 100%;
					height: 100%;
				}
			}
			.chat-text{
				padding: 10rpx;
				border-radius: 10rpx;
				color: #fff;
				background-color: #1AAD19;
			}
			.chat-content-left{
				padding: 20upx;
			}
			.chat-content-right{
				justify-content: flex-end;
				padding: 20upx;
			}
		}
		.chat-input{
			height: $input-height;
			// background-color: #007AFF;
			// padding:10rpx;
			align-items:center;
			.input{
				height: 30rpx;
				padding: 8rpx 15rpx;
				font-size: 26rpx;
				line-height: 30rpx;
				margin-right: 20rpx;
				border: 2rpx solid #eee;
			}
		}
	}
</style>
