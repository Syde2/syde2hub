<script setup>
const props = defineProps({
	id: String,
	title: String,
	label: String,
	image: String,
	checked:Boolean

})
</script>

<template>
	<div class="container">
		<input type="radio" name="slide" :id="props.id" :checked="props.checked" >
		<label :for="props.id" class="card" :style="{ 'background-image': 'url(' + props.image + ')' }">
			<div class="row">
				<div class="icon">	{{ props.id }} </div>		
				<div class="description">
					<h4> {{ props.title }} </h4>
					<p> {{ props.label }} </p>
				</div>
			</div>
		</label>
	</div>
</template>


<style scoped>
.container {
	height: 400px;
	display: flex;
	flex-wrap: nowrap;
	justify-content: start;
}

.card {
	width: 80px;
	border-radius: .75rem;
	background-size: cover;
	cursor: pointer;
	overflow: hidden;
	border-radius: 2rem;
	margin: 0 10px;
	display: flex;
	align-items: flex-end;
	transition: .6s cubic-bezier(.28, -0.03, 0, .99);
	box-shadow: 0px 10px 30px -5px rgba(0, 0, 0, 0.8);
}

.card>.row {
	color: white;
	display: flex;
	flex-wrap: nowrap;
	align-items: end;
}

.card>.row>.icon {
	background: #2E3440;
	color: white;
	border-radius: 50%;
	width: 50px;
	height: 50px;
	display: flex;
	justify-content: center;
	align-items: center;
	margin: 15px;
}

.card>.row>.description {
	display: flex;
	justify-content: center;
	flex-direction: column;
	overflow: hidden;
	height: 230px;
	width: 520px;
	opacity: 0;
	transform: translateY(30px);
	transition-delay: .3s;
	transition: all .3s ease;
}

.description p {
	color: white;
}

.description h4 {
	text-transform: uppercase;
	font-size: 3rem;
}

input {
	display: none;
}

input:checked+label {
	width: 600px;
}

input:checked+label .description {
	opacity: 1 !important;
	transform: translateY(0) !important;
}

</style>

