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

		<div class="row justify-between" v-show="!mobile">
			<q-parallax
				src="https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/christopher-gower-m_HRfLhgABo-unsplash.jpg?alt=media"
			>
			</q-parallax>
		</div>
		<q-footer elevated bordered v-show="mobile">
			<a href="">teste1</a>
			<a href="">teste2</a>
			<a href="">teste3</a>
		</q-footer>
	</div>
</template>

<script>
	export default {
		name: "PageIndex",
		data() {
			return {
				slide: 1,
				mobile: false,
			};
		},
		mounted() {
			this.$q.platform.is.mobile ? (this.mobile = true) : (this.mobile = false);
		},
	};
</script>
