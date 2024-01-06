<script setup>
import IllustrationCard from './IllustrationCard.vue';

const data = [
	{
		id:'P', 
		title: 'Projects',
		image:'/img1.jpeg', 
		label: ' "It takes half your life before you discover life is a do-it-yourself project."- Napoleon Hill ',
		checked:true
	},
	{
		id: 'A', 
		title: 'About Me',
		image:'/img2.jpeg', 
		label: ' "Tell me and I forget. Teach me and I remember. Involve me and I learn." - Benjamin Franklin',
		checked:false
	},
	{
		id:'H', 
		title: 'Hobbies',
		image:'/img3.jpeg', 
		label: '"Where words fail, music speaks."- Hans Andersen ',
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
