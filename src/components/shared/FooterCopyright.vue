<script>
export default {
	data: () => {
		return {
			copyrightDate: new Date().getFullYear(),
			projectName: 'Ana Paula Parizotto Design',
			author: 'uxduda',
		};
	},
};
</script>

<template>
	<div class="flex justify-center items-center text-center">
		<div
			class="font-general-regular text-lg text-ternary-dark dark:text-ternary-light"
		>
			&copy; {{ copyrightDate }}
			<a
				href="https://github.com/realstoman/vuejs-tailwindcss-portfolio"
				target="__blank"
				class="font-general-medium hover:underline hover:text-pink-600 dark:hover:text-pink-300 duration-500"
			>
				{{ projectName }}
			</a>
			- desenvolvido por
			<a
				href="https://uxduda.com"
				target="__blank"
				class="font-general-medium text-secondary-dark dark:text-secondary-light hover:underline hover:text-pink-600 dark:hover:text-pink-300 duration-500"
				>{{ author }}</a
			>
		</div>
	</div>
</template>

<style lang="scss" scoped></style>
