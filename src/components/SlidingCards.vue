<script setup>
</script>

<template>
	<div class="wrapper">
		<div class="container">
			<input type="radio" name="slide" id="c1" checked>
			<label for="c1" class="card">
				<div class="row">
					<div class="icon">I</div>
					<div class="description my-font">
						<h4>Faery</h4>
						<p>Faery comes with creativity</p>
					</div>
				</div>
			</label>

			<input type="radio" name="slide" id="c2">
			<label for="c2" class="card">
				<div class="row">
					<div class="icon">II</div>
					<div class="description">
						<h4>Digital Technology</h4>
						<p>Gets better every day -
							stay tuned</p>
					</div>
				</div>
			</label>

			<input type="radio" name="slide" id="c3">
			<label for="c3" class="card">
				<div class="row">
					<div class="icon">III</div>
					<div class="description">
						<h4>Globalization</h4>
						<p>Help people all over the world</p>
					</div>
				</div>
			</label>

			<input type="radio" name="slide" id="c4">
			<label for="c4" class="card">
				<div class="row">
					<div class="icon">IV</div>
					<div class="description">
						<h4>New technologies</h4>
						<p>Space engineering becomes
							more and more advanced</p>
					</div>
				</div>
			</label>
			
		</div>
	</div>
</template>

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    font-family: Arial, Helvetica, sans-serif;
}

body {
    background-color: #eeeeea;
}

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
    transition: .6s cubic-bezier(.28,-0.03,0,.99);
    box-shadow: 0px 10px 30px -5px rgba(0,0,0,0.8);
}

.card > .row {
    color: #2E3440;
    display: flex;
    flex-wrap: nowrap;
}

.card > .row > .icon {
    background: rgba(255, 255, 255, 0.8);
    color: black;
    border-radius: 50%;
    width: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 15px;
	font-family: 'satoshi';
}

.card > .row > .description {
    display: flex;
    justify-content: center;
    flex-direction: column;
    overflow: hidden;
    height: 80px;
    width: 520px;
    opacity: 0;
    transform: translateY(30px);
    transition-delay: .3s;
    transition: all .3s ease;
	font-family: 'satoshi';

}

.description p {
    color: #2E3440;
    padding-top: 5px;
	font-family: 'satoshi';

}

.description h4 {
    text-transform: uppercase;
}

input {
    display: none;
}

input:checked + label {
    width: 600px;
}

input:checked + label .description {
    opacity: 1 !important;
    transform: translateY(0) !important;
}

.card[for="c1"] {
    background-image: url('/img1.webp');
}
.card[for="c2"] {
    background-image: url('/img2.webp');
}
.card[for="c3"] {
    background-image: url('/img3.webp');
}
.card[for="c4"] {
    background-image: url('/img4.jpeg');
}
</style>