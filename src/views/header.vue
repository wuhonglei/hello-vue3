<template>
	<div class="header-wrapper relative">
		<!-- 顶部导航 -->
		<nav class="top-navigation py-5">
			<div class="nav-container h-full flex justify-between items-center flex-wrap">
				<a
					href="/"
					class="brand-text text-white text-xl font-bold"
				>EchoCloud回声云</a>
				<button
					class="py-1 px-3 md:hidden"
					@click="showLinks=!showLinks"
				>
					<i class="fas fa-bars text-white"></i>
				</button>
				<div class="flex w-full md:flex-1 justify-between items-center">
					<ul
						class="flex-1 flex flex-col md:flex-row link-container pl-0 md:pl-8 bg-white md:bg-transparent md:text-white"
						:class="[showLinks ? 'link-container-show': 'link-container-hidden']"
					>
						<li
							v-for="item in menus"
							:key="item.name"
						>
							<a
								:href="item.href"
								class="nav-link"
							>{{item.name}}</a>
						</li>
					</ul>
					<button class="hidden md:inline-block user-center rounded-full bg-white">
						<i class="fab fa-fort-awesome mr-2 text-xs"></i>
						<span>用户中心</span>
					</button>
				</div>
			</div>
		</nav>
		<!-- 内容展示 -->
		<div class="site-desc mt-4 flex justify-between">
			<div class="flex-1 flex flex-col items-center md:items-start text-white pt-12 md:pt-15 md:mr-20">
				<div class="mb-10 rounded-full recent-activity flex items-center text-xs">
					<span class="mr-1 py-px px-1 rounded-full bg-red-600">New</span>
					年付8折优惠活动，限时进行中
				</div>
				<div class="text-4xl mb-2">全球网络加速服务，随时随地使用</div>
				<div class="mt-4 text-md">通过我们的网络访问内容提供商、公司网络和公共云服务</div>
				<button class=" shadow-xl mt-10 rounded-full py-3 px-8 bg-orange-400 text-base">开始使用</button>
			</div>
			<div class="hidden md:block md:flex-1">
				<img
					class="w-full h-full"
					src="https://echo99.com/theme/malio/index/landing/ill.svg"
					alt=""
				>
			</div>
		</div>
	</div>
</template>

<script>

/**
 * 顶部导航以及网页介绍
 */

import { reactive, ref } from 'vue';
export default {
	setup() {
		const menus = reactive([{
			name: '特性',
			href: '#features'
		}, {
			name: '价格',
			href: '#purchase'
		}, {
			name: '支持',
			href: '#contact-support'
		}]);

		const showLinks = ref(true);

		return {
			menus,
			showLinks
		}
	}
}
</script>

<style lang="postcss" scoped>
.header-wrapper {
	font-size: 14px;
}

.top-navigation {
	height: 81px;
}

.brand-text {
	letter-spacing: 3px;
}

.fa-bars {
	font-size: 13px;
}

.nav-link {
	display: flex;
	align-items: center;
	height: 34px;
	box-sizing: border-box;
	padding: 3px 20px;
	font-size: 14px;
}

.link-container {
	transition: height 1s ease;
}

.link-container-hidden {
	height: 0;
	overflow: hidden;
}

.link-container-show {
	height: auto;
}

.user-center {
	height: 41px;
	padding: 7px 25px;
	box-sizing: border-box;
}

.site-desc {
	height: 470px;
}

.recent-activity {
	background-color: rgba(255, 255, 255, 0.2);
	padding: 5px 10px;
	cursor: pointer;
}
</style>