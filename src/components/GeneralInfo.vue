<template>
	<v-container>
		<div id="my_avatar">
			<img src="../assets/images/self/me.png" alt="Yogaraj.S" />
		</div>
		<div id="my_name">
			<h1>Yogaraj Sivaprakasam</h1>
		</div>
		<div id="my_designation">
			<h3>Full Stack/Python Developer</h3>
		</div>
		<div id="my_location">
			<img src="../assets/images/social_media/location-pin.svg" alt="Location" />
			<h5>Puducherry, India</h5>
		</div>
	</v-container>
</template>

<script>
export default {
	data() {
		return {
			social_links: [
				{
					id: 1,
					src: "../assets/images/social_media/stack-overflow.svg",
					link: "",
				},
				{
					id: 2,
					src: "../assets/images/social_media/email.svg",
					link: "",
				},
				{
					id: 3,
					src: "../assets/images/social_media/linkedin.svg",
					link: "",
				},
				{
					id: 4,
					src: "../assets/images/social_media/github.svg",
					link: "",
				},
				{
					id: 5,
					src: "../assets/images/social_media/twitter.svg",
					link: "",
				},
				{
					id: 6,
					src: "../assets/images/social_media/instagram.svg",
					link: "",
				},
			],
		};
	},
};
</script>

<style lang="scss" scoped>
#my_avatar {
	padding: 1em;
	text-align: center;
}

#my_name {
	font-family: Roboto;
	font-style: normal;
	font-weight: bold;
	display: flex;
	align-items: center;
	text-align: center;
	letter-spacing: 0.06em;
	color: #000000;
	text-shadow: 1px 2px 5px rgba(0, 0, 0, 0.25);

	h1 {
		margin: 0 auto;
	}
}

#my_designation {
	margin-top: 10px;
	font-family: Roboto;
	font-style: normal;
	font-size: 18px;
	line-height: 21px;
	text-align: center;
	letter-spacing: 0.04em;
	color: #000000;

	h3 {
		margin: 0 auto;
	}
}

#my_location {
	text-align: center;
	line-height: 21px;
	margin-top: 10px;
	display: flex;
	justify-content: center;

	img {
		width: 25px;
		height: 25px;
	}

	h5 {
		font-family: Roboto;
		font-style: normal;
		font-weight: bold;
		font-size: 14px;
		line-height: 16px;
		display: flex;
		align-items: center;
		letter-spacing: 0.06em;
	}
}
</style>