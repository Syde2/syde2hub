<script setup>
const props = defineProps(['data'])
const {id, title, label, image, checked, to} = props.data
</script>

<template>
	<div class="container">
		<input type="radio" name="slide" :id="id" :checked="checked" >
		<label :for="id" class="card" :style="{ 'background-image': 'url(' + image + ')' }">
			<div class="fit  row text-white">
				<div class=" flex justify-center items-end ">
					<h4 class="title"> {{ title }} </h4>
					<div class="icon ">{{ id }} </div>		
				</div>

			</div>
			<div class="description col-8  " @click="()=>$router.push(to) " >
					<p class="ellipsis-3-lines"> {{ label }} </p>
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
	width: 100px;
	border-radius: .75rem;
	background-size: cover;
	background-position: center;
	cursor: pointer;
	overflow: hidden;
	border-radius: 2rem;
	margin: 0 10px;
	display: flex;
	align-items: flex-end;
	transition: .6s cubic-bezier(.28, -0.03, 0, .99);
	box-shadow: 0px 10px 30px -5px rgba(0, 0, 0, 0.8);
}

.icon {
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
.description {
	padding: 1rem;
	overflow: hidden;
	height: 100%;
	width: 100%;
	display: flex;
	justify-content: center;
	align-items: end;
	font-weight: 500;
	font-size: 1.2rem;
	letter-spacing: 1.2px;
	opacity: 0;
	transform: translateY(30px);
	transition-delay: .3s;
	transition: all .3s ease;
}

.description p {
	color: white;
	width: 80%;
	text-overflow: ellipsis;
	margin-right: 1rem;
	background-color: rgba(35, 33, 33, 0.549);
	padding: 0.5rem;
	padding-bottom: 0.1rem;
}

.title {
	text-transform: uppercase;
	font-size: 2.8rem;
	writing-mode: vertical-rl;
	text-orientation: sideways-right;
	margin: 10px;
	font-weight: 600;
	max-height: 300px;
}

input {
	display: none;
}

input:hover+label{
	opacity: 0.9;
}

input:checked+label {
	width: 600px;
	max-width: 70vw;
}
input:active+label {
	transform: perspective(800px) rotateX(20deg) rotateY(0deg);
}

input:checked+label .description {
	opacity: 1 !important;
	transform: translateY(0) !important;

}

input:checked+label .title {
color: rgba(255, 255, 255, 0.9);

}



</style>

