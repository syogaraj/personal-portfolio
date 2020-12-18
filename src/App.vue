<template>
	<v-app>
		<v-app-bar app dark>
			<div class="d-flex align-center">
				<h2>Yogaraj Sivaprakasam</h2>
			</div>

			<v-spacer></v-spacer>
			<div id="nav_links">
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
			<v-container>
				<router-view></router-view>
			</v-container>
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
};
</script>

<style scoped lang="scss">
#nav_links > a {
	text-decoration: none;
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
</style>