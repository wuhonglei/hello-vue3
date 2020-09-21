<template>
	<div class="header-wrapper">
		<!-- 顶部导航 -->
		<nav class="top-navigation py-5 px-4">
			<div class="nav-container h-full flex justify-between items-center">
				<a
					href="/"
					class="brand-text text-white text-xl font-bold"
				>EchoCloud回声云</a>
				<button class="py-1 px-3">
					<i class="fas fa-bars text-white"></i>
				</button>
			</div>
		</nav>
	</div>
</template>

<script>
export default {

}
</script>

<style lang="postcss" scoped>
.header-wrapper {
	height: 500px;
	background-image: linear-gradient(to bottom, #697ded, #5e30c1);
}

.top-navigation {
	height: 81px;
}

@media screen and (min-width: 1024;) {
	.top-navigation {
		padding-left: 69px;
		padding-right: 69px;
	}
}

.nav-container {
	margin: 0 34px;
}

.brand-text {
	letter-spacing: 3px;
}

.fa-bars {
    font-size: 13px;
}
</style>