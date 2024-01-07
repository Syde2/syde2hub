<script setup>
import { ref } from 'vue'
const slide = ref(1)
</script>

<template>
	<div class="q-pa-md" style="width:80vw; " >

		<q-carousel animated v-model="slide" arrows thumbnails infinite :autoplay="5000"  >
			<q-carousel-slide :name="1" img-src="img1.jpeg" />
			<q-carousel-slide :name="2" img-src="img2.jpeg" />
			<q-carousel-slide :name="3" img-src="img3.jpeg" />
		</q-carousel>

	</div>
</template>
  
