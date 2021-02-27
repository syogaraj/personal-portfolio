<template>
	<v-card elevation="9">
		<v-card-title>Work Experience</v-card-title>
		<v-card-subtitle>How's it going so far!</v-card-subtitle>
		<v-divider />
		<v-expansion-panels>
			<v-expansion-panel
				v-for="(company, index) in companies"
				:key="index"
			>
				<v-expansion-panel-header>
					<template v-slot:actions>
						<v-icon color="primary"> $expand </v-icon>
					</template>
					<v-img
						class="tw-mr-4"
						style="max-width: 64px !important"
						:src="company.icon"
						width="50"
					/>
					{{ company.name }}
				</v-expansion-panel-header>
				<v-expansion-panel-content>
					<v-list
						v-for="(text, textIndex) in company.workExp"
						:key="textIndex"
					>
						{{ text }}
						<v-divider />
					</v-list>
				</v-expansion-panel-content>
			</v-expansion-panel>
		</v-expansion-panels>
	</v-card>
</template>

<script>
export default {
	data() {
		return {
			companies: [
				{
					name: "Zoho Corporation Pvt. Ltd  (2017 - Present)",
					icon: require("../assets/images/programming_languages/zoho.png"),
					workExp: [
						"Responsible for Python application which collects data from machines which drives the cloud environment of Zoho.",
						"Rewritten the python application to establish a solid data-driven logic with maintainability.",
						"Increased the efficiency of python application by 40%.",
						"Migrated the python application codebase from python2 to python3.",
						"Migrated front-end views from jQuery to Vue.js framework.",
						"Modelled and Scaled MySQL to handle large amount of data efficiently.",
						"Co-ordinate with teams to understand their application use case and incorporate them in the python monitoring application.",
						"Understand and analyze Linux kernel for better and efficient monitoring of the system and incorporate it in the python application.",
						"Trained and managed team of two developers and discussed issues in order to provide resolution and apply best practices.",
						"Implemented process improvements to smooth development cycle and increase collaboration.",
					],
				},
			],
		};
	},
};
</script>

<style>
</style>