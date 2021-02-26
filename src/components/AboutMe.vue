<template>
	<div id="aboutMe">
		<div id="self_descr" class="elevation-20">
			<p>
				<strong>Hey, there!</strong>
			</p>
			<p>
				I'm Yogaraj from Puducherry, India.
				<br />I love programming, problem solving and I'm currently working as a Full Stack and Python Developer at Zoho.
				<br />Feel free to get in touch or take a look at my past work below.
				<br />
			</p>
		</div>
	</div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
#aboutMe {
	color: white;
}

#self_descr {
	background: linear-gradient(
			to left,
			#ffffff 0%,
			rgba(82, 255, 224, 0.816901) 0.01%,
			rgba(255, 255, 255, 0) 100%
		),
		#169dff;
	padding: 1.5em;
	border-radius: 2em;
	max-width: 70%;
	margin: 0 auto;
	font-size: 1.35rem;
	font-weight: 300;

	p:nth-child(2) {
		margin-left: 3em;
		font-weight: bolder;
		@media (max-width: 425px) {
			margin-left: 1em;
		}
	}
}
</style>