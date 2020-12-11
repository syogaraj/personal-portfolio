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
				<router-link to="/about">
					<v-btn depressed>About me</v-btn>
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
</style>