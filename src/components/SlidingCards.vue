<script setup>
import IllustrationCard from './IllustrationCard.vue';
</script>

<template>
	<div class="container flex no-wrap justify-start" style="height: 25vw;" >

		<IllustrationCard :checked="true" id='I' title="Alan Wake" image='/img1.jpeg'
			label="An FBI agent looking for answers. Two realities. Two hero characters.
			One horror story that wants them dead." />

		<IllustrationCard id='II' title="Control" image='/img2.jpeg'
			label="Supernatural third-person action-adventure game will challenge you to
			master a combination of supernatural abilities, modifiable loadouts and reactive environments" />

		<IllustrationCard id='III' title="Quantum Break" image='/img3.jpeg'
			label="Time itself becomes fractured in a time travel experiment, Jack Joyce fights the secretive
			Monarch Solutions to put things right before it’s too late." />

		<IllustrationCard id='VI' title="Max Payne" image='/img4.jpeg'
			label=" Max is a man with his back against the wall, fighting a battle he cannot hope to win." />

	</div>
</template>
