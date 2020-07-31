<template>

<div id="item" @click="onVideoSelect">
	<section>
		<img :src="thumbnailUrl">
	</section>
	
</div>
		
	
</template>

<script>
export default {
	name: 'VideoItem',
	props: {
		video: Object
	},
	computed: {
		thumbnailUrl() {
			return this.video.snippet.thumbnails.default.url;
		}
	},
	methods: {
		onVideoSelect() {
			this.$emit('videoSelect', this.video);
		}
	}
}
</script>

<style scoped>
	


h4{
	display: inline-block;
}
img{
	width: 186px;
	height: 118px;
}


</style>