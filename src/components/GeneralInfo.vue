<template>
	<v-container>
		<section>
			<div id="my_avatar">
				<img
					src="../assets/images/self/me.png"
					class="tw-border-8 tw-rounded-full tw-shadow-2xl"
					alt="Yogaraj.S"
				/>
			</div>
			<div id="my_name">
				<h1>Yogaraj Sivaprakasam</h1>
			</div>
			<v-divider light></v-divider>
			<div id="my_designation">
				<h3>Full Stack/Python Developer</h3>
			</div>
			<div id="my_location">
				<img
					src="../assets/images/social_media/location-pin.svg"
					alt="Location"
				/>
				<h5>Puducherry, India</h5>
			</div>
			<div
				id="my_social_media"
				class="tw-hidden md:tw-flex md:tw-justify-between md:tw-w-9/12 lg:tw-w-6/12"
			>
				<div
					v-for="item in social_links"
					:key="item.id"
					@click="openLink(item)"
				>
					<v-tooltip bottom>
						<template v-slot:activator="{ on, attrs }">
							<v-img
								:src="item.src"
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
			<div class="tw-flex tw-justify-between tw-w-9/12 md:tw-hidden" id="mob_social_media">
				<div
					v-for="item in mobSocialLinks"
					:key="item.id"
					@click="openLink(item)"
				>
					<v-tooltip bottom>
						<template v-slot:activator="{ on, attrs }">
							<v-img
								:src="item.src"
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
				<v-btn depressed rounded large @click="$emit('get-started')"
					>Let's get started!</v-btn
				>
			</div>
		</section>
	</v-container>
</template>

<script>
export default {
	data() {
		return {
			mobSocialLinks: [
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
			],
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
	font-size: 1.75em;
	display: flex;
	align-items: center;
	text-align: center;
	letter-spacing: 0.04em;

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

#my_social_media, #mob_social_media {
	margin: 0 auto;
	padding-top: 5em;

	.v-image {
		border-radius: 50%;

		&:hover {
			box-shadow: 0px 6px 7px -4px rgba(0, 0, 0, 0.2),
				0px 11px 15px 1px rgba(0, 0, 0, 0.14),
				0px 4px 20px 3px rgba(0, 0, 0, 0.12) !important;
			cursor: pointer;
			@apply tw--mt-3;
		}
	}
}

#get_started {
	text-align: center;
	padding-top: 9em;

	button {
		color: white;
		background-color: #272727;
	}
}
</style>