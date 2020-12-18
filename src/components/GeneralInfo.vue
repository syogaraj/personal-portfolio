<template>
	<v-container>
		<div id="my_avatar">
			<v-avatar size="158">
				<img src="../assets/images/self/me.png" alt="Yogaraj.S" />
			</v-avatar>
		</div>
		<div id="my_name">
			<h1>Yogaraj Sivaprakasam</h1>
		</div>
		<div id="my_designation">
			<h3>Full Stack/Python Developer</h3>
		</div>
		<!-- <div id="my_location"></div> -->
	</v-container>
</template>

<script>
export default {
	data() {
		return {};
	},
};
</script>

<style lang="scss" scoped>
#my_avatar {
	padding: 1em;
	text-align: center;

	.v-avatar {
		box-shadow: 0px 4px 9px 2px rgba(109, 119, 120, 0.84);
		border-radius: 100px;

		img {
			width: 11em;
			margin-top: 8px;
			height: 11em;
		}
	}
}

#my_name {
	font-family: Roboto;
	font-style: normal;
	font-weight: bold;
	display: flex;
	align-items: center;
	text-align: center;
	letter-spacing: 0.06em;
	color: #000000;
	text-shadow: 1px 2px 5px rgba(0, 0, 0, 0.25);

	h1 {
		margin: 0 auto;
	}
}

#my_designation {
	margin-top: 10px;
	font-family: Roboto;
	font-style: normal;
	font-size: 18px;
	line-height: 21px;
	text-align: center;
	letter-spacing: 0.04em;
	color: #000000;

	h3 {
		margin: 0 auto;
	}
}
</style>