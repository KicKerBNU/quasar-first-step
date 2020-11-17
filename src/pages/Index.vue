<template>
	<div class="q-pa-md q-gutter-md container">
		<q-card
			class="my-card"
			style="background: radial-gradient(circle, #EBEBF3 0%, #FFFF 100%)"
		>
			<q-card-section>
				<h5>Hi, im a Frontend developer</h5>
				<p>
					All you find on this website is done with VueJS, a Javascript
					framework focused on building SPA.
				</p>
				<p>Hope you enjoy, fell free to contact me anytime</p>
			</q-card-section>
		</q-card>

		<div class="row justify-between">
			<q-parallax
				src="https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/christopher-gower-m_HRfLhgABo-unsplash.jpg?alt=media"
			>
			</q-parallax>
		</div>
		<q-card
			class="my-card text-white vertical-middle"
			style="background: radial-gradient(circle, #35a2ff 0%, #014a88 100%)"
		>
			<q-card-section class="flex flex-center">
				<div class="text-h6">
					Keep studing, keep learning and never give up!
				</div>
			</q-card-section>
			<img alt="VueJS" src="~assets/vuejs.jpg" />

			<!-- <q-card-section class="q-pt-none">
				<img alt="Everton photo" src="~assets/everton_t.png" />
			</q-card-section> -->
		</q-card>
		<q-page> </q-page>
	</div>
</template>

<script>
	export default {
		name: "PageIndex",
	};
</script>
<style scoped>
	.container {
		margin: 2%;
	}
</style>
