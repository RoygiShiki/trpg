<template>
	<div class="home">
		<filecard></filecard>
	</div>
</template>

<script>
	// @ is an alias to /src
	import filecard from '@/components/filecard.vue';

	export default {
		name: 'Home',
		components: {
			filecard
		}
	}
</script>
