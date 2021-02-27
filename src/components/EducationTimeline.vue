<template>
	<v-card elevation="9">
		<v-card-title>Education</v-card-title>
		<v-card-subtitle>It all started from here!</v-card-subtitle>
		<v-divider />
		<v-timeline dense>
			<v-timeline-item
				v-for="(item, index) in education"
				:key="index"
				:color="item.color"
				:icon="item.icon"
			>
				<v-card class="tw-w-11/12">
					<v-card-title style="word-break: break-word">{{
						item.name
					}}</v-card-title>
					<v-card-subtitle>{{ item.stream }}</v-card-subtitle>
					<v-card-text>{{ item.mark }}</v-card-text>
				</v-card>
			</v-timeline-item>
		</v-timeline>
	</v-card>
</template>

<script>
export default {
	data() {
		return {
			education: [
				{
					name: "Sri Manakula Vinayagar Engineering College",
					stream: "Majored in Information Technology (2017)",
					mark: "CGPA: 9.1/10",
					icon: "mdi-school-outline",
				},
				{
					name: "Achariya Siksha Mandir",
					stream: "HSC - Maths, Physics, Biology (2013)",
					mark: "Percentage: 82.8%",
					color: "#97b83f",
					icon: "mdi-book-check-outline",
				},
				{
					name: "Vivekananda Higher Secondary School",
					stream: "SSLC (2011)",
					mark: "Percentage: 94%",
					icon: "mdi-buffer",
					color: "#ff84c5",
				},
			],
		};
	},
};
</script>

<style>
</style>