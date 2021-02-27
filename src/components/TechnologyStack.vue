<template>
	<v-card elevation="10">
		<v-card-title>Technology Stack</v-card-title>
		<v-divider></v-divider>
		<div class="tw-p-3">
			<v-chip
				outlined
				class="ma-2"
				color="indigo"
				v-for="(tech, index) in techStack"
				:key="index"
			>
				<v-avatar left>
					<v-img :src="tech.imgSrc" width="70" />
				</v-avatar>
				{{ tech.name }}
			</v-chip>
		</div>
	</v-card>
</template>

<script>
export default {
	data() {
		return {
			techStack: [
				{
					name: "Python",
					imgSrc: require("../assets/images/programming_languages/python.png"),
				},
				{
					name: "Java",
					imgSrc: require("../assets/images/programming_languages/java.png"),
				},
				{
					name: "Linux",
					imgSrc: require("../assets/images/programming_languages/linux.png"),
				},
				{
					name: "Vue.js",
					imgSrc: require("../assets/images/programming_languages/vue.png"),
				},
				{
					name: "Vuetify",
					imgSrc: require("../assets/images/programming_languages/vuetify.png"),
				},
				{
					name: "JavaScript",
					imgSrc: require("../assets/images/programming_languages/javascript.png"),
				},
				{
					name: "HTML",
					imgSrc: require("../assets/images/programming_languages/html.png"),
				},
				{
					name: "CSS",
					imgSrc: require("../assets/images/programming_languages/css.png"),
				},
				{
					name: "MySQL",
					imgSrc: require("../assets/images/programming_languages/mysql.png"),
				},
				{
					name: "NodeJS",
					imgSrc: require("../assets/images/programming_languages/nodejs.png"),
				},
				{
					name: "Tailwind CSS",
					imgSrc: require("../assets/images/programming_languages/tailwind.png"),
				},
				{
					name: "Python-Flask",
					imgSrc: require("../assets/images/programming_languages/python_flask.png"),
				},
			],
		};
	},
};
</script>

<style>
</style>