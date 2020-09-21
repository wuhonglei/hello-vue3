<template>
	<div class="header-wrapper">
		<!-- 顶部导航 -->
		<nav class="top-navigation my-5 mx-4">
            <div class="flex justify-between">
                <a href="/">EchoCloud回声云</a>
                <i class="fas fa-bars"></i> 
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
    background-image: linear-gradient(to bottom, var(--purple), var(--indigo));
}

.top-navigation {
	height: 81px;
	line-height: 41px;
}

@media screen and (min-width: 1024;) {
    .top-navigation {
        padding-left: 69px;
        padding-right: 69px;
    }
}
</style>