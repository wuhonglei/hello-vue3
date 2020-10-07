<template>
	<div class="wrapper mt-20">
		<div
			class="flex mt-20"
			v-for="item in list"
			:key="item.src"
		>
			<div class="hidden md:block w-4/12 mr-12">
				<img
					class="w-full h-auto"
					:src="item.src"
					alt=""
				>
			</div>
			<section class="flex-1">
				<p class="title inline-block mb-4">{{item.title}}</p>
				<h2 class="mb-2">{{item.subtitle}}</h2>
				<p class="lead">{{item.desc}}</p>
			</section>
		</div>
		<div class="flex mt-20">
			<div class="hidden md:block w-8/12 mr-12">
				<img
					class="portait h-full"
					src="https://echo99.com/theme/malio/index/img/waiting_notifications.svg"
					alt=""
				>
			</div>
			<section class="flex-1">
				<p class="title inline-block mb-4">不仅仅如此，亦包含以下诸多特性</p>
				<h2 class="mb-2">* 部分特性需要配合第三方客户端与托管规则使用</h2>
				<div class="lead">
					<div
						class="flex mb-6"
						v-for="item in features"
						:key="item.name"
					>
						<!-- 左侧方形图标 -->
						<div class="feature-icon text-white mr-5">
							<i :class="['fas', item.icon]"></i>
						</div>
						<!-- 右侧文字描述 -->
						<div class="flex-1 text-14px more-feature-title">
							{{item.title}}
						</div>
					</div>
				</div>
			</section>
		</div>
	</div>
</template>

<script>
export default {
	setup() {
		let list = [{
			src: 'https://echo99.com/theme/malio/index/img/data_center.svg',
			title: 'CROSS DEVICES & PLATFORMS',
			subtitle: '在你心爱的电子设备中使用，无论是移动的手机还是固定的电脑，随时随处可用',
			desc: 'EchoCloud回声云国际网络加速的服务适用于 macOS、iOS、Android、Windows 和 Linux，借助第三方客户端，可在手机、电脑、路由器、游戏机、电视盒子中使用。'
		}, {
			src: 'https://echo99.com/theme/malio/index/img/netflix.png',
			title: 'UNBLOCK STREAMING MEDIA',
			subtitle: '加速游戏，加速海外网课速度',
			desc: '通过 EchoCloud回声云国际网络加速 的服务，可以畅连海外游戏，加速网课连接速度'
		}];
		let features = [{
			icon: 'fa-ad',
			title: '过滤常用网站广告、常用视频广告、其他网站广告'
		}, {
			icon: 'fa-filter',
			title: '智能分流系统，所有国内网站直线连接，增强用户体验'
		}, {
			icon: 'fa-apple-alt',
			title: 'Apple服务加速 (App Store、Apple Music、iCloud、iTunes等)'
		}, {
			icon: 'fa-tachometer-alt',
			title: '国外常用网站加速 (Google/Youtube/Twitter/Instgram/Github等)'
		}, {
			icon: 'fa-lock',
			title: '在传输过程中使用最强的加密方式，保护用户数据和隐私'
		}, {
			icon: 'fa-fire',
			title: '与诸多平台上的优秀应用程序兼容，这些应用程序由许多创新公司和开发人员开发'
		}];
		return {
			list,
			features
		}
	}
}
</script>

<style lang="postcss" scoped>
.title {
	padding: 7px 12px;
	line-height: 1;
	border-radius: 30px;
	font-size: 12px;
	color: white;
	background-color: var(--text);
}

.lead {
	padding: 16px 0;
}

.wrapper > div:nth-of-type(even) {
	flex-direction: row-reverse;
}

.portait {
	width: 480px;
}

.feature-icon {
	display: flex;
	width: 50px;
	height: 50px;
	background-color: var(--text);

	& .fas {
		margin: auto;
		font-size: 22px;
	}
}

.more-feature-title {
	color: #4e5051;
}
</style>