<script setup>
import IllustrationCard from './IllustrationCard.vue';

const data = [
	{
		id:1, 
		title: 'Projects',
		image:'/img1.jpeg', 
		label: '',
		checked:true
	},
	{
		id:2, 
		title: 'About Me',
		image:'/img2.jpeg', 
		label: 'lorem Ipsum',
		checked:false
	},
	{
		id:3, 
		title: 'Hobbies',
		image:'/img3.jpeg', 
		label: 'lorem Ipsum',
		checked:false
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
