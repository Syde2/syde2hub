<script setup>
import IllustrationCard from './IllustrationCard.vue';

const data = [
	{
		id:0, 
		title: 'title',
		image:'/img1.webp', 
		label: 'lorem Ipsum',
		checked:true
	},
	{
		id:1, 
		title: 'title',
		image:'/img2.webp', 
		label: 'lorem Ipsum',
		checked:true
	},
	{
		id:3, 
		title: 'title',
		image:'/img3.webp', 
		label: 'lorem Ipsum',
		checked:true
	}
]

</script>

<template>
	<div class="container flex no-wrap justify-start" style="height: 25vw;" >
		<div v-for="each in data" :key="each.id"   >
			<IllustrationCard  :data="each"   />
		</div>


	</div>
</template>
