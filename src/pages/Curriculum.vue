<template>
	<div class="q-pa-lg">
		<q-timeline :layout="layout" :side="side" color="secondary">
			<q-timeline-entry heading>{{ currentYear }}</q-timeline-entry>

			<q-timeline-entry
				title="Masterlink Business Innovation"
				:subtitle="currentJob"
				side="right"
				avatar="https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/Masterlink_03.PNG?alt=media"
			>
				<div>Frontend Developer</div>
			</q-timeline-entry>

			<q-timeline-entry
				title="Inventti Soluções"
				subtitle="Mai 15, 2022"
				side="right"
				avatar="https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/iventti.png?alt=media"
			>
				<div>Frontend Developer</div>
				<div>Projects: Grid System, Omni Channel</div>
			</q-timeline-entry>

			<q-timeline-entry
				title="Inventti Soluções"
				subtitle="June 05, 2020"
				side="right"
				avatar="https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/iventti.png?alt=media"
			>
				<div>Junior Frontend Developer</div>
				<div>Projects: Transport Invoices, ERP Accountant Area</div>
			</q-timeline-entry>

			<q-timeline-entry heading>2019</q-timeline-entry>

			<q-timeline-entry
				title="Inventti Soluções"
				subtitle="December 05, 2019"
				side="right"
				avatar="https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/iventti.png?alt=media"
			>
				<p>ERP Software</p>
				<div>
					Intership: Development of front end interfaces using VueJs.
				</div>
				<div>Projects: Referral Marketing, POS, Onboarding</div>
			</q-timeline-entry>

			<q-timeline-entry
				title="Be Sistemas"
				subtitle="May, 2019 - December 2019"
				side="left"
				avatar="https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/besistemas.jpg?alt=media"
			>
				<p>Mall Management Software</p>
				<div>
					Customer Success, Unit Testing, Software Documentation, Bug Fixes
				</div>
			</q-timeline-entry>
		</q-timeline>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				layout: "comfortable",
				side: "right",
				currentYear: null,
				currentJob: null,
			};
		},
		mounted() {
			this.getCurrentYear();
		},
		methods: {
			getCurrentYear() {
				var now = new Date();
				this.currentYear = now.getFullYear();

				const monthNames = [
					"January",
					"February",
					"March",
					"April",
					"May",
					"June",
					"July",
					"August",
					"September",
					"October",
					"November",
					"December",
				];

				this.currentJob =
					monthNames[now.getMonth()] +
					" " +
					now.getDate() +
					", " +
					this.currentYear +
					" - Current job ";
			},
		},
	};
</script>

<style></style>
