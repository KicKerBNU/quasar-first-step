<template>
	<div class="container">
		<div class="row">
			<div
				class="col-xs-12 col-sm-6 col-md-4"
				v-for="stack in stackList"
				:key="stack.id"
			>
				<q-card class="size-img">
					<a :href="stack.url" target="_blank">
						<q-img :src="stack.image" basic>
							<div class="absolute-bottom text-subtitle2 text-center">
								{{ stack.title }}
							</div>
						</q-img>
					</a>
				</q-card>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				stackList: [
					{
						id: 1,
						title: "VueJs",
						image:
							"https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/vuejs3.jpg?alt=media",
						url: "https://v3.vuejs.org/guide/introduction.html",
					},
					{
						id: 2,
						title: "Quasar",
						image:
							"https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/quasar.jpg?alt=media",
						url: "https://quasar.dev/start/pick-quasar-flavour",
					},
					{
						id: 3,
						title: "Materialize",
						image:
							"https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/materialize.png?alt=media",
						url: "https://materializecss.com/",
					},
					{
						id: 4,
						title: "Git",
						image:
							"https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/git_.jpg?alt=media",
						url: "https://git-scm.com//",
					},
					{
						id: 5,
						title: "Github",
						image:
							"https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/github.jpg?alt=media",
						url: "https://github.com/",
					},
					{
						id: 6,
						title: "Gitlab",
						image:
							"https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/gitlab.png?alt=media",
						url: "https://gitlab.com/",
					},
					{
						id: 7,
						title: "Firebase",
						image:
							"https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/firebase.jpg?alt=media",
						url: "https://firebase.google.com/",
					},
					{
						id: 8,
						title: "DevTools",
						image:
							"https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/devtools.jpg?alt=media",
						url: "https://developers.google.com/web/tools/chrome-devtools",
					},
					{
						id: 9,
						title: "CSS3",
						image:
							"https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/css3.jpg?alt=media",
						url: "https://devdocs.io/css/",
					},
					{
						id: 10,
						title: "HTML5",
						image:
							"https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/html5.jpg?alt=media",
						url: "https://devdocs.io/html/",
					},
					{
						id: 11,
						title: "PUG",
						image:
							"https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/pug.png?alt=media",
						url: "https://pugjs.org/api/reference.html",
					},
					{
						id: 12,
						title: "Hotjar",
						image:
							"https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/hotjar.png?alt=media",
						url: "https://hotjar.com",
					},
				],
			};
		},
	};
</script>

<style></style>
