<template>
	<div>
		<section class="home">
			<GeneralInfo @get-started="getStarted()" />
		</section>
		<section class="about" ref="about">
			<AboutMe />
		</section>
	</div>
</template>

<script>
// @ is an alias to /src
import GeneralInfo from "@/components/GeneralInfo.vue";
import AboutMe from "@/components/AboutMe.vue";

export default {
	name: "Home",
	components: { GeneralInfo, AboutMe },
	methods: {
		getStarted() {
			console.log("getting started");
			this.$refs["about"].scrollIntoView({
				behavior: "smooth",
				block: "end",
				inline: "nearest",
			});
		},
	},
};
</script>

<style lang="scss" scoped>
.home {
	min-height: 100vh !important;
}

.about {
	min-height: 90vh !important;
}
</style>
