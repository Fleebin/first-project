<template>
  <div id="item" @click="onVideoSelect">
    <img :src="thumbnailUrl" />
    <div class="descricao">
	{{ video.snippet.title }}
	</div>
  </div>
</template>

<script>
export default {
  name: "VideoItem",
  props: {
    video: Object,
  },
  computed: {
    thumbnailUrl() {
      return this.video.snippet.thumbnails.default.url;
    },
  },
  methods: {
    onVideoSelect() {
      this.$emit("videoSelect", this.video);
    },
  },
};
</script>

<style scoped>

#item{
	display: flex;
 	
	align-content : flex-end;
	
	background-color: #FFFFFF;

	margin-bottom: 32px;
	border-radius: 6px;

	padding: 30px;
}
img {
  width: 100px;
  height: 80px;

  margin-right:32px;
}
@media (min-width:768px){
  #item{
	display: block;
 	
	
	
	background-color: #FFFFFF;

	margin-bottom: 32px;
	border-radius: 6px;

	padding: 30px;
}
img {
  width: 60px;
  height: 60px;

  margin-right:32px;
}
}
</style>