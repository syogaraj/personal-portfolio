<template>
	<div id="aboutMe">
		<v-card
			class="elevation-11 rounded-lg theme--light tw-mt-14 tw-mx-auto tw-w-11/12 md:tw-w-8/12 lg:tw-w-4/12 tw-p-3"
		>
			<v-card-title>About Me</v-card-title>
			<v-card-subtitle
				>Full Stack/Python Developer with 3+ years of
				experience</v-card-subtitle
			>
			<v-card-text style="font-size: 1rem; letter-spacing: 0.03rem">
				Experienced full stack developer with broad skills in developing
				complex application. Skills include Vue.js, Python, Linux, Java.
				Strong engineering professional with a Bachelor's degree in the
				stream of Information Technology.
			</v-card-text>
		</v-card>
		<div id="comprehensiveStack">
			<div id="techStack" class="comprehensiveDiv">
				<tech-stack />
			</div>
			<div id="workExp" class="comprehensiveDiv">
				<work-experience />
			</div>
			<div id="education" class="comprehensiveDiv">
				<education-timeline />
			</div>
		</div>
	</div>
</template>

<script>
import TechStack from "./TechnologyStack.vue";
import EducationTimeline from "./EducationTimeline.vue";
import WorkExperience from "./WorkExperience.vue";
export default {
	components: { TechStack, EducationTimeline, WorkExperience },
};
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

#comprehensiveStack {
	@apply tw-flex tw-flex-col xl:tw-flex-row tw-p-3 tw-justify-center tw-mt-11;
	.comprehensiveDiv {
		@apply tw-w-11/12 tw-mx-auto tw-my-4 md:tw-w-8/12 xl:tw-mx-3;
	}

	#techStack {
		@apply xl:tw-mt-16;
	}

	#education {
		@apply xl:tw-mt-10;
	}
}
</style>