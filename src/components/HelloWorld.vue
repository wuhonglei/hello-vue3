<template>
	<div>
		<h1>{{ msg }}</h1>
		<button @click="count++">count is: {{ count }}</button>
		<p>Edit <code>components/HelloWorld.vue</code> to test hot module replacement.</p>
	</div>
</template>

<script>

let person = {};
console.info(person?.name ?? 'wuhonglei');

export default {
	  name: "HelloWorld",
	props: {
		msg: String
	},
	data() {
		return {
			count: 0
		}
	}
}
</script>
