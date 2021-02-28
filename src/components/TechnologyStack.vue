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
					imgSrc: require("../assets/images/techstack/python.png"),
				},
				{
					name: "Java",
					imgSrc: require("../assets/images/techstack/java.png"),
				},
				{
					name: "Linux",
					imgSrc: require("../assets/images/techstack/linux.png"),
				},
				{
					name: "Vue.js",
					imgSrc: require("../assets/images/techstack/vue.png"),
				},
				{
					name: "Vuetify",
					imgSrc: require("../assets/images/techstack/vuetify.png"),
				},
				{
					name: "JavaScript",
					imgSrc: require("../assets/images/techstack/javascript.png"),
				},
				{
					name: "HTML",
					imgSrc: require("../assets/images/techstack/html.png"),
				},
				{
					name: "CSS",
					imgSrc: require("../assets/images/techstack/css.png"),
				},
				{
					name: "MySQL",
					imgSrc: require("../assets/images/techstack/mysql.png"),
				},
				{
					name: "NodeJS",
					imgSrc: require("../assets/images/techstack/nodejs.png"),
				},
				{
					name: "Tailwind CSS",
					imgSrc: require("../assets/images/techstack/tailwind.png"),
				},
				{
					name: "Python-Flask",
					imgSrc: require("../assets/images/techstack/python_flask.png"),
				},
				{
					name: "Git",
					imgSrc: require("../assets/images/techstack/git.png"),
				},
			],
		};
	},
};
</script>

<style>
</style>