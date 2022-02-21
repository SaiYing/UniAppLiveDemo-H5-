<template>
	<view class="content">
		<view class="video-js" ref="video">

		</view>
	</view>
</template>

<script>
	export default {
		onReady() {
			// #ifdef H5
			var video = document.createElement('video')
			video.id = 'video'
			video.style = 'width: 300px;height: 150px;'
			video.controls = true
			var source = document.createElement('source')
			source.src =
				'http://220.161.87.62:8800/hls/0/index.m3u8'
			video.appendChild(source)
			this.$refs.video.$el.appendChild(video)
			videojs('video')
			// #endif
		},
		methods: {

		}
	}
</script>

<style>
	
</style>
