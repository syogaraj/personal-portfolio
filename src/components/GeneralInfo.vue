<template>
	<v-container>
		<section>
			<div id="my_avatar">
				<img src="../assets/images/self/me.png" alt="Yogaraj.S" />
			</div>
			<div id="my_name">
				<h1>Yogaraj Sivaprakasam</h1>
			</div>
			<v-divider light></v-divider>
			<div id="my_designation">
				<h3>Full Stack/Python Developer @Zoho</h3>
			</div>
			<div id="my_location">
				<img src="../assets/images/social_media/location-pin.svg" alt="Location" />
				<h5>Puducherry, India</h5>
			</div>
			<div id="my_social_media">
				<div v-for="item in social_links" :key="item.id">
					<v-tooltip bottom>
						<template v-slot:activator="{ on, attrs }">
							<v-img
								:src="item.src"
								@click="openLink(item)"
								width="60"
								height="60"
								v-on="on"
								v-bind="attrs"
							/>
						</template>
						<span>{{ item.tooltip }}</span>
					</v-tooltip>
				</div>
			</div>
			<div id="get_started">
				<v-btn depressed rounded large>Let's get started!</v-btn>
			</div>
		</section>
	</v-container>
</template>

<script>
export default {
	data() {
		return {
			social_links: [
				{
					id: 1,
					src: require("../assets/images/social_media/stack-overflow.svg"),
					link: "https://stackoverflow.com/users/3607028/yogaraj",
					tooltip: "StackOverflow",
				},
				{
					id: 2,
					src: require("../assets/images/social_media/email.svg"),
					link: "mailto:yogarajsivaprakasam@gmail.com",
					tooltip: "Email",
				},
				{
					id: 3,
					src: require("../assets/images/social_media/linkedin.svg"),
					link: "https://www.linkedin.com/in/syogaraj",
					tooltip: "LinkedIn",
				},
				{
					id: 4,
					src: require("../assets/images/social_media/github.svg"),
					link: "https://www.github.com/syogaraj",
					tooltip: "Github",
				},
				{
					id: 5,
					src: require("../assets/images/social_media/twitter.svg"),
					link: "https://www.twitter.com/_yogarajs",
					tooltip: "Twitter",
				},
				{
					id: 6,
					src: require("../assets/images/social_media/instagram.svg"),
					link: "https://www.instagram.com/_yogarajs",
					tooltip: "Instagram",
				},
			],
		};
	},
	methods: {
		openLink(item) {
			window.open(item.link, "_blank");
		},
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

hr {
	width: 33%;
	margin: 0 auto;
	border-top: solid 4px;
	padding-bottom: 0.5em;
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
	padding-top: 5px;

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

#my_social_media {
	width: 45%;
	display: flex;
	justify-content: space-between;
	margin: 0 auto;
	padding-top: 5em;
}

#get_started {
	text-align: center;
	padding-top: 9em;

	button {
		color: white;
		background-color: #e51256;
	}
}
</style>