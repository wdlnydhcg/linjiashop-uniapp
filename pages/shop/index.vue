<template>
	<view>
		<!-- 轮播海报 -->
		<view class="placard-wrap-card">
			<u-swiper borderRadius="0" height="1480" class="placard-swiper" mode="none" :list="nav_list" interval="3000" ></u-swiper>
		</view>
		<!-- 会员 -->
		<view class="member-wrap-card">
			<view class="member-info">
				<image src="https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/menber_bg.jpg"></image>
				<view class="member-info-text">
					<view class="member-info-name">张三</view>
					<view class="member-info-score">599</view>
				</view>
				<u-swiper borderRadius="0" img-mode="aspectFit" height="450" mode="none" :list="member_list" interval="3000" ></u-swiper>
			</view>
			<u-image width="100%" height="229rpx" src="https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/nav/menber_title.jpg"></u-image>
			<u-image width="100%" height="580rpx" src="https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/nav/menber_content.jpg"></u-image>
			
		</view>
		<!-- 甄选产品 -->
		<view class="carefully-wrap-card">
			<u-image width="100%" height="188rpx" src="https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/home_select.jpg"></u-image>			
			<view class="carefully-nav">
				<u-row class="placeholder">
					<u-col span="3" @click="changeCurCarefullyIndex(0)"><view style="height:120rpx"></view></u-col>
					<u-col span="3" @click="changeCurCarefullyIndex(1)"><view style="height:120rpx"></view></u-col>
					<u-col span="3" @click="changeCurCarefullyIndex(2)"><view style="height:120rpx"></view></u-col>
					<u-col span="3" @click="changeCurCarefullyIndex(3)"><view style="height:120rpx"></view></u-col>
				</u-row>
				<view class="background">
					<u-image v-show="curCarefullyIndex === 0" :src="carefully_nav_list[0]" mode="aspectFit" height="128rpx" width="100%"></u-image>
					<u-image v-show="curCarefullyIndex === 1" :src="carefully_nav_list[1]" mode="aspectFit" height="128rpx" width="100%"></u-image>
					<u-image v-show="curCarefullyIndex === 2" :src="carefully_nav_list[2]" mode="aspectFit" height="128rpx" width="100%"></u-image>
					<u-image v-show="curCarefullyIndex === 3" :src="carefully_nav_list[3]" mode="aspectFit" height="128rpx" width="100%"></u-image>
				</view>
			</view>
			<u-swiper @change="changeCurCarefullyIndex" :current='curCarefullyIndex' borderRadius="0" height="1158" mode="none" :list="carefully_product_list" interval="3000" ></u-swiper>
		</view>
		<!-- 甄选产品2 -->
		<view class="carefully2-wrap-card">
			<u-image width="100%" height="188rpx" src="https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/home_select_2.jpg"></u-image>
			
			
			<view class="carefully2-content-wrap">
				<u-image width="100%" height="1146rpx" src="https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/carefully2_select_1.jpg"></u-image>
				<view class="carefully2_content1_wrap">
					<image class="carefully2_content1_item" mode="heightFix" height="478rpx" src="https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/carefully2_content5.png"></image>
					
				</view>
			</view>
			<view class="carefully2-content-wrap">
				<u-image width="100%" height="1146rpx" src="https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/carefully2_select_2.jpg"></u-image>
				<view class="carefully2_content1_wrap">
					<image class="carefully2_content1_item" mode="heightFix" height="478rpx" src="https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/carefully2_content2.png"></image>
				</view>
			</view>
			<view class="carefully2-content-wrap">
				<u-image width="100%" height="1146rpx" src="https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/carefully2_select_3.jpg"></u-image>
				<view class="carefully2_content1_wrap">
					<image class="carefully2_content1_item" mode="heightFix" height="478rpx" src="https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/carefully2_content3.png"></image>
				</view>
			</view>
			<view class="carefully2-content-wrap">
				<u-image width="100%" height="1146rpx" src="https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/carefully2_select_4.jpg"></u-image>
				
				<view class="carefully2_content1_wrap">
					<image class="carefully2_content1_item" mode="heightFix" height="478rpx" src="https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/carefully2_content4.png"></image>
				</view>
			</view>
			<view class="carefully2-content-wrap">
				<u-image width="100%" height="1146rpx" src="https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/carefully2_select_5.jpg"></u-image>
				<view class="carefully2_content1_wrap">
					<image class="carefully2_content1_item" mode="heightFix" height="478rpx" src="https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/carefully2_content1.png"></image>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				nav_list: [{
						image: 'https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/nav/nav_1.jpg',
					},
					{
						image: 'https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/nav/nav_2.jpg',
					},
					{
						image: 'https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/nav/nav_3.jpg',
					},
					{
						image: 'https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/nav/nav_4.jpg',
					},
					{
						image: 'https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/nav/nav_5.jpg',
					},
					{
						image: 'https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/nav/nav_6.jpg',
					}
				],
				member_list: [{
						image: 'https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/nav/menber_nav_1.jpg',
					},{
						image: 'https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/nav/menber_nav_3.jpg',
					},
				],
				curCarefullyIndex:0,
				carefully_nav_list: [
					 'https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/carefully_select_1.jpg',
					 'https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/carefully_select_2.jpg',
					 'https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/carefully_select_3.jpg',
					 'https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/carefully_select_4.jpg',
				],
				carefully_product_list: [
					{
						image: 'https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/home_1.jpg',
					},{
						image: 'https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/home_2.jpg',
					},{
						image: 'https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/home_3.jpg',
					},{
						image: 'https://zhong-1257747316.cos.ap-guangzhou.myqcloud.com/home/home_4.jpg',
					}
				],
				
				imgUrl:""

			}
		},
		onLoad() {

		},
		onShow(){

		},
		methods: {
			changeCurCarefullyIndex(index){
				this.curCarefullyIndex = index
			}
		}

	}
</script>

<style lang="scss" scoped>
	
	.placard-wrap-card{
		.u-swiper-wrap{
			border-radius: 0;
		}
	}
	.member-wrap-card{
		.member-info{
			width: 100%;
			position: relative;
			image{
				position: absolute;
				left: 0;
				top: 0;
				width: 750rpx;
				height: 308rpx;
				z-index: 0;
			}
			.member-info-text{
				position: relative;
				height: 308rpx;
				z-index:1;
				.member-info-name{
					position: absolute;
					bottom: 138rpx;
					left: 250rpx;
				}
				.member-info-score{
					position: absolute;
						bottom: 94rpx;
						left: 310rpx;
					
				}
			}
		}
	}
	.carefully-wrap-card{		
		.carefully-nav{
			position: relative;
			height: 128rpx;
			.placeholder{
				height: 128rpx;
			}
			.background{
				position: absolute;
				width: 100%;
				top: 0%;
				left: 0%;
				z-index: -1;
			}
		}
	}
	.carefully2-wrap-card{
		.carefully2-content-wrap{
			position: relative;
			.carefully2_content1_wrap{
				position: absolute;
				bottom: 0;
				width: 100%;
				height:478rpx;
				overflow-x: auto;
				.carefully2_content1_item{
					// height: 100%;
				}
			}
		}
	}
</style>
