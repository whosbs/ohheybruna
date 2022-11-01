<script>
import AppBanner from '@/components/shared/AppBanner';
import ProjectsGrid from '../components/projects/ProjectsGrid.vue';
// import Button from '../components/reusable/Button.vue';

export default {
	name: 'Home',
	components: {
		AppBanner,
		ProjectsGrid,
		// Button,
	},
};
</script>

<template>
	<div class="container mx-auto">
		<!-- Banner -->
		<AppBanner class="mb-5 sm:mb-8" />

		<!-- Projects -->
		<ProjectsGrid />

		<!-- Load mais projetos button OCULTO -->
		<!-- <div class="mt-10 sm:mt-20 flex justify-center">
			<router-link
				to="/projects"
				class="font-general-medium flex items-center px-6 py-3 rounded-lg shadow-lg hover:shadow-xl bg-pink-500 hover:bg-pink-600 focus:ring-1 focus:ring-pink-900 text-white text-lg sm:text-xl duration-300"
				aria-label="mais projetos"
			>
				<Button title="mais projetos" />
			</router-link>
		</div> -->
	</div>
</template>

<style scoped></style>
