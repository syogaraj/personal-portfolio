<template>
	<v-app>
		<v-app-bar app dark class="tw-hidden md:tw-block">
			<div class="d-flex align-center">
				<h2 class="md:tw-flex">Yogaraj Sivaprakasam</h2>
			</div>

			<v-spacer></v-spacer>
			<div id="nav_links" class="tw-hidden">
				<router-link to="/home">
					<v-btn depressed>Home</v-btn>
				</router-link>
				<router-link to="/projects">
					<v-btn depressed>Projects</v-btn>
				</router-link>
				<router-link to="/portfolio">
					<v-btn depressed>Portfolio</v-btn>
				</router-link>
			</div>
		</v-app-bar>

		<v-main>
			<router-view
				class="tw-bg-gradient-to-tr tw-from-pink-300 tw-to-green-200 tw-via-yellow-200"
			></router-view>
		</v-main>
	</v-app>
</template>

<script>
export default {
	name: "App",

	components: {},

	data: () => ({
		//
	}),

	metaInfo: {
		title: "Yogaraj.S - Personal Portfolio",
		meta: [
			{ charset: "utf-8" },
			{ name: "description", content: "Personal portfoio of Yogaraj.S" },
			{
				property: "og.description",
				content: "Personal portfolio of Yogaraj.S",
			},
			{ property: "og:title", content: "Yogaraj.S - Personal Portfolio" },
			{ property: "og:site_name", content: "Yogaraj.S" },
			{ property: "og:type", content: "website" },
			{ property: "og:image", content: require("./assets/images/self/me.png")},
			{ name: "robots", content: "index,follow" },
		],
	}
};
</script>

<style scoped lang="scss">
@font-face {
	font-family: "Varela";
	src: local("Varela"),
		url(./fonts/varela/Varela-Regular.ttf) format("truetype");
}
@font-face {
	font-family: "Nunito";
	src: local("Nunito"),
		url(./fonts/nunito/Nunito-Regular.ttf) format("truetype");
}

#nav_links > a {
	text-decoration: none;
	@apply tw-hidden md:tw-block;
}
.router-link-active > button {
	background: white !important;
	color: black;
}

#app {
	background: linear-gradient(
			180deg,
			#cff0fb 19.27%,
			rgba(245, 252, 254, 0.208696) 75.52%,
			rgba(255, 255, 255, 0) 94.79%
		),
		#eaf7ff;
	mix-blend-mode: normal;
	border: 1px solid #e7d3d3;
	box-sizing: border-box;
}

.v-main {
	@apply tw-p-0 #{!important} md:tw-pt-16 #{!important};
}
</style>