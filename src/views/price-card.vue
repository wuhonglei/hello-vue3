<template>
	<section class="py-32">
		<div class="text-center px-6">
			<h2 class="text-white">出色的体验，意想不到的价格</h2>
			<p class="lead my-5">不要把宝贵的时间，浪费在等待上。即刻开启全球网络中继服务，在任何时间任何地点访问全球互联网。</p>
		</div>
		<div class="flex mt-12 flex-wrap">
			<div
				class="flex-1 mt-2 mx-4 rounded-sm bg-white text-center pricing"
				v-for="version in Object.keys(price)"
				:key="version"
			>
				<div class="pricing-title bg text-primary text-10px font-bold">
					{{price[version].title}}
				</div>
				<div class="p-10 text-secondary flex flex-col items-center">
					<div>
						<p class="pricing-price">{{price[version].price}}</p>
						<p class="text-14px font-normal">每月</p>
					</div>
					<div class="pricing-details text-14px font-normal">
						<div
							class="flex mb-4"
							v-for="item in price[version].details"
							:key="item.desc"
						>
							<div
								class="feature-icon text-xs"
								:class="[item.enable ? 'enable' : 'disable']"
							>
								<i :class="['fas m-auto', item.enable ? 'fa-check' : 'fa-times']"></i>
							</div>
							<div class="desc">
								{{item.desc}}
							</div>
						</div>
					</div>
				</div>
				<div class="pricing-cta mt-5 bg flex items-center justify-center text-14px font-bold text-primary">
					<a class="mr-3">订阅</a>
					<i class="fas fa-arrow-right"></i>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	setup() {
		let price = {
			standard: {
				title: '标准版(轻度需求购买这个)',
				price: '￥19.99',
				details: [{
					enable: true,
					desc: '70GB 使用流量'
				}, {
					enable: true,
					desc: '2个 在线客户端'
				}, {
					enable: true,
					desc: '在线客服有限技术支持'
				}, {
					enable: true,
					desc: '国际标准节点'
				}, {
					enable: false,
					desc: '国内国际高速节点'
				}, {
					enable: false,
					desc: 'IPLC专线极速节点'
				}]
			},
			professional: {
				title: '高级版(网课等速度需求购买这个)',
				price: '￥29.99',
				details: [{
					enable: true,
					desc: '150GB 使用流量'
				}, {
					enable: true,
					desc: '3个 在线客户端'
				}, {
					enable: true,
					desc: '在线客服有限技术支持'
				}, {
					enable: true,
					desc: '国际标准节点'
				}, {
					enable: true,
					desc: '国内国际高速节点'
				}, {
					enable: false,
					desc: 'IPLC专线极速节点'
				}]
			},
			enhanced: {
				title: '加强版（暂不开放购买，请不要下单）',
				price: '￥39.99',
				details: [{
					enable: true,
					desc: '300GB 使用流量'
				}, {
					enable: true,
					desc: '6个 在线客户端'
				}, {
					enable: true,
					desc: '在线客服有限技术支持'
				}, {
					enable: true,
					desc: '国际标准节点'
				}, {
					enable: true,
					desc: '国内国际高速节点'
				}, {
					enable: true,
					desc: 'IPLC专线极速节点'
				}]
			}
		};

		return {
			price
		};
	}
}
</script>

<style lang="postcss" scoped>
.lead {
	color: rgba(255, 255, 255, 0.5);
}

.bg {
	background-color: #f3f6f8;
}

.pricing-title {
	padding: 5px 15px;
}

.pricing-price {
	font-size: 50px;
}

.pricing-details {
	margin-top: 45px;
}

.feature-icon {
	display: flex;
	width: 20px;
	height: 20px;
	border-radius: 50%;
	margin-right: 10px;
	color: white;
}

.enable {
	background-color: #6574f7;
}

.disable {
	background-color: #98a6ad;

	& + .desc {
		color: #98a6ad;
		text-decoration: line-through;
	}
}

.pricing-cta {
	width: 100%;
	height: 61px;
	cursor: pointer;
	transition: all 0.5s;

	&:hover {
		color: #0056b3;
		background-color: #e3eaef;
	}
}
</style>