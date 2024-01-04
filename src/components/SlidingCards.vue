<script setup>
import IllustrationCard from './IllustrationCard.vue';
</script>

<template>
	<div class="container flex no-wrap justify-start" style="height: 25vw;" >
		<IllustrationCard :checked="true" id='I' title="Dream" image='/img1.webp'
			label="Space engineering becomes more and more advanced" />
		<IllustrationCard id='II' title="Dream" image='/img2.webp'
			label="Space engineering becomes more and more advanced" />
		<IllustrationCard id='III' title="Dream" image='/img3.webp'
			label="Space engineering becomes more and more advanced" />
		<IllustrationCard id='VI' title="Dream" image='/img4.webp'
			label="Space engineering becomes more and more advanced" />

	</div>
</template>
