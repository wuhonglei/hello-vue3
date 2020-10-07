<template>
	<div class="bg-white font-semibold">
		<div class="header-wrapper">
			<i-header class="container mx-auto"></i-header>
		</div>
		<div class="container mx-auto">
			<glories-card></glories-card>
			<feature-card></feature-card>
			<introduce-card></introduce-card>
		</div>
		<!-- 价格列表 -->
		<div class="server-wrapper">
			<price-card class="container mx-auto"></price-card>
		</div>
	</div>
</template>

<script>
import iHeader from './views/header.vue';
import GloriesCard from './views/glories-card.vue';
import FeatureCard from './views/feature-card.vue';
import IntroduceCard from './views/introduce-card.vue';
import PriceCard from './views/price-card.vue';

export default {
	name: 'App',
	components: {
		iHeader,
		GloriesCard,
		FeatureCard,
		IntroduceCard,
		PriceCard
	}
}
</script>

<style lang="postcss" scoped>
.header-wrapper {
	background-image: linear-gradient(to bottom, #697ded, #5e30c1);
}

.server-wrapper {
	background-image: linear-gradient(to top, #697ded, #5e30c1);
}
</style>
