<script setup>
import IllustrationCard from './IllustrationCard.vue';
</script>

<template>
	<div class="wrapper">
		<div class="container">
			<IllustrationCard id='I' title="Dream" image='/img1.webp'
				label="Space engineering becomes more and more advanced" />
			<IllustrationCard id='II' title="Dream" image='/img2.webp'
				label="Space engineering becomes more and more advanced" />
			<IllustrationCard id='III' title="Dream" image='/img3.webp'
				label="Space engineering becomes more and more advanced" />
			<IllustrationCard id='VI' title="Dream" image='/img4.jpeg'
				label="Space engineering becomes more and more advanced" />

		</div>
	</div>
</template>

<style>
.wrapper {
	width: 100%;
	height: 100vh;
	display: flex;
	align-items: center;
	justify-content: center;
}

.container {
	height: 400px;
	display: flex;
	flex-wrap: nowrap;
	justify-content: start;
}</style>