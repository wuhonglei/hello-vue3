<template>
	<section class="mt-32">
		<div class="text-center">
			<h2 class="whitespace-normal">
				为你<span class="text-primary mx-2">量身定制</span>
				<span class="text-primary">的服务</span>
			</h2>
			<p class="py-4 lead">可靠的基础设置，并能提供您喜爱的诸多功能</p>
		</div>
		<div class="mt-16 grid grid-cols-3">
			<div
				class="flex flex-col"
				v-for="item in list"
				:key="item.id"
			>
				<div class="feature-icon rounded-full mb-5 text-primary">
					<i :class="['fas', item.icon]"></i>
				</div>
				<p class="text-xl">{{item.title}}</p>
				<p class="py-4 text-base leading-8 desc font-normal">{{item.desc}}</p>
			</div>
		</div>
	</section>
</template>

<script>

/**
 * 网站特性描述
 */

export default {
	setup() {
		let list = [{
			icon: 'fa-mobile-alt',
			title: '高速稳定',
			desc: '体验宛若身在海外的访问速度'
		}, {
			icon: 'fa-code',
			title: '便携设置',
			desc: '我们的服务适用于 macOS、iOS、Android、Windows 和 Linux'
		}, {
			icon: 'fa-fire',
			title: '节省成本',
			desc: '相比自托管服务可节省大量费用'
		}, {
			icon: 'fa-check',
			title: '全球互联',
			desc: '通过 IXP 连接至全球内容提供商，更加快速'
		}, {
			icon: 'fa-columns',
			title: '运营商友好',
			desc: '我们的产品和您的当地运营商兼容，适用于您的固网与移动网络'
		}, {
			icon: 'fa-chevron-right',
			title: '多应用兼容',
			desc: '提供全面且可靠的第三方应用程序兼容'
		}];
		return {
			list
		}
	}
}
</script>

<style lang="postcss" scoped>
.desc {
	color: #4e5051;
}

.feature-icon {
	display: flex;
	width: 50px;
	height: 50px;
	background-color: rgba(103, 119, 239, 0.1);

	& .fas {
		margin: auto;
		font-size: 22px;
	}
}
</style>