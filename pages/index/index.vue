<template>
	<view class="content">
		<view class="title">
			2023年部分考生初试成绩查询
		</view>
		<view class="sming">
			<view> 招生单位说明: 我校对考生初试成绩不作排名，请勿来电询问有关排名情况。其他考试相关信息请关注我校研究生招生信息网相关公告。</view>
		</view>
		<view class="main-box">
			<template v-for="(item,index) in list" :key="index">
				<view class="list">
					<text class="biaoti">{{item.tile}}</text><text class="nr">{{item.con}}</text>
				</view>
			</template>

		</view>
		<view class="xiam">
			<view>本系统所有数据均为招生单位提供，招生单位对查询结果负责解释。</view>
			<view>若查询的成绩为负值，表示有缺考、违纪等情况。若仍对查询结果有疑问，请咨询相应的招生单位。</view>
		</view>
		<view class="" style="height: 90rpx;"></view>
		<view class="xfk">
			返回
		</view>
	</view>
</template>

<script setup>
	import {
		ref
	} from "vue";

	let list = ref([{
			tile: '姓名',
			con: '完成者'
		},
		{
			tile: '报名号',
			con: '370271898'
		},
		{
			tile: '准考证号',
			con: '445224200004211812'
		},
		{
			tile: '总分',
			con: '322'
		},
		{
			tile: '第一门',
			con: '(101)思想政治理论: 51'

		},
		{
			tile: '第二门',
			con: '(101)英语 (二) : 36'
		},
		{
			tile: '第三门',
			con: '(101)数学 (二) : 95'
		},
		{
			tile: '第四门',
			con: '(852)信号与系统或数据结构: 51'
		},
		{
			tile: '备注',
			con: '无'
		}
	])
</script>

<style lang="scss">
	page {
		background-color: #F6F6F6;
	}

	@font-face {
		font-family: 'ht';
		src: url('../../static/fzht.TTF') format('truetype');
	}

	.content {
		font-family: ht;

		.title {
			height: 85rpx;
			background-color: #4A91E3;
			display: flex;
			justify-content: center;
			align-items: center;
			font-size: 35rpx;
			color: #fff;
		}

		.sming {
			background-color: #F6F6F6;
			padding-bottom: 45rpx;

			view {
				padding: 20rpx;
				color: #5B584F;
				background-color: #FEFBEC;
				font-size: 29rpx;
			}

		}

		.main-box {
			background-color: #fff;

			.list {
				border-top: 2rpx solid #E5E5E5;

				display: flex;
				// align-items: center;
				padding: 30rpx 20rpx;
				font-size: 35rpx;

				.biaoti {
					color: #3D3D3D;
					width: 190rpx;

				}

				.nr {
					color: #B9B9B9;
					flex: 1;
				}
			}
		}

		.xiam {
			padding: 20rpx 20rpx;
			background-color: #F6F6F6;

			view {
				margin-top: 15rpx;
				font-size: 29rpx;
				color: #9D9D9D;
			}
		}

		.xfk {
			background-color: #4A91E1;
			color: #fff;
			position: fixed;
			bottom: 0;
			left: 20rpx;
			right: 20rpx;
			display: flex;
			justify-content: center;
			align-items: center;
			height: 90rpx;
			font-size: 36rpx;
			border-top-left-radius: 6rpx;
			border-top-right-radius: 6rpx;
		}
	}
</style>
