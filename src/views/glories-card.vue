<template>
	<div class="w-full wrapper flex flex-col md:flex-row shadow-xl">
		<div class="flex-1 mr-4">
			<p class="text-gray-500 mb-1 tracking-widest">为什么选择 ECHOCLOUD 回声云国际网络加速</p>
			<div class="text-8">
				<p class="bar-border">迄今为止</p>
			</div>
		</div>
		<div class="flex-1 flex justify-between">
			<div
				class="reason-item"
				v-for="item in list"
				:key="item.desc"
			>
				<p class="mb-2 text-8">{{item.count}}</p>
				<p class="text-primary">{{item.desc}}</p>
			</div>
		</div>
	</div>
</template>

<script>

/**
 * 头部的卡片成就介绍
 */

export default {
	setup() {
		let list = [{
			count: '20+',
			desc: '国际节点'
		}, {
			count: '10+',
			desc: '国家地区'
		}, {
			count: '700+',
			desc: '满意用户'
		}];
		return {
			list
		}
	}
}
</script>

<style lang="postcss" scoped>
.wrapper {
	padding: 60px 50px;
	font-size: 14px;
}

.text-8 {
	font-size: 32px;
}

.bar-border::before {
	float: left;
	margin-top: 30px;
	margin-right: 16px;
	content: "";
	width: 50px;
	height: 8px;
	border-radius: 4px;
	background-color: var(--text);
}
</style>