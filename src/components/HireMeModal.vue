<script>
import feather from 'feather-icons';
import Button from './reusable/Button.vue';
export default {
	props: ['showModal', 'modal', 'categories'],
	components: { Button },
	data() {
		return {};
	},
	mounted() {
		feather.replace();
	},
	updated() {
		feather.replace();
	},
	methods: {},
};
</script>

<template>
	<transition name="fade">
		<div v-show="modal" class="font-general-regular fixed inset-0 z-30">
			<!-- Modal body background as backdrop -->
			<div
				v-show="modal"
				@click="showModal()"
				class="bg-filter bg-black bg-opacity-50 fixed inset-0 w-full h-full z-20"
			></div>
			<!-- Modal content -->
			<main
				class="flex flex-col items-center justify-center h-full w-full"
			>
				<transition name="fade-up-down">
					<div
						v-show="modal"
						class="modal-wrapper flex items-center z-30"
					>
						<div
							class="modal max-w-md mx-5 xl:max-w-xl lg:max-w-xl md:max-w-xl bg-secondary-light dark:bg-primary-dark max-h-screen shadow-lg flex-row rounded-lg relative"
						>
							<div
								class="modal-header flex justify-between gap-10 p-5 border-b border-ternary-light dark:border-ternary-dark"
							>
								<h5
									class=" text-primary-dark dark:text-primary-light text-xl"
								>
									Que tipo de projeto você precisa?
								</h5>
								<button
									class="px-4 text-primary-dark dark:text-primary-light"
									@click="showModal()"
								>
									<i data-feather="x"></i>
								</button>
							</div>
							<div class="modal-body p-5 w-full h-full">
								<form class="max-w-xl m-4 text-left">
									<div class="mt-0">
										<input
											class="w-full px-5 py-2 border-1 border-gray-200 dark:border-secondary-dark rounded-md text-md bg-secondary-light dark:bg-ternary-dark text-primary-dark dark:text-ternary-light"
											id="name"
											name="name"
											type="text"
											required=""
											placeholder="Nome"
											aria-label="Nome"
										/>
									</div>
									<div class="mt-6">
										<input
											class="w-full px-5 py-2 border-1 border-gray-200 dark:border-secondary-dark rounded-md text-md bg-secondary-light dark:bg-ternary-dark text-primary-dark dark:text-ternary-light"
											id="email"
											name="email"
											type="text"
											required=""
											placeholder="Email"
											aria-label="Email"
										/>
									</div>
									<div class="mt-6">
										<select
											class="w-full px-5 py-2 border-1 border-gray-200 dark:border-secondary-dark rounded-md text-md bg-secondary-light dark:bg-ternary-dark text-primary-dark dark:text-ternary-light"
											id="subject"
											name="subject"
											type="text"
											required=""
											aria-label="Categoria do Projeto"
										>
											<option
												v-for="category in categories"
												:key="category.id"
												:value="category.value"
												>{{ category.name }}</option
											>
										</select>
									</div>

									<div class="mt-6">
										<textarea
											class="w-full px-5 py-2 border-1 border-gray-200 dark:border-secondary-dark rounded-md text-md bg-secondary-light dark:bg-ternary-dark text-primary-dark dark:text-ternary-light"
											id="message"
											name="message"
											cols="14"
											rows="6"
											aria-label="Detalhes"
											placeholder="Descrição do projeto"
										></textarea>
									</div>
								</form>
							</div>
							<div
								class="modal-footer mt-2 sm:mt-0 py-5 px-8 border0-t text-right"
							>
										<Button
											title="enviar"
											class="px-4
											sm:px-6
											py-2
											sm:py-2.5
											text-white
											bg-pink-500
											hover:bg-pink-600
											rounded-md
											focus:ring-1 focus:ring-pink-900 duration-500"
											type="submit"
											aria-label="Submit Request"
										/>
							</div>
						</div>
					</div>
				</transition>
			</main>
		</div>
	</transition>
</template>

<style scoped>
.modal-body {
	max-height: 500px;
}
.bg-gray-800-opacity {
	background-color: #2d374850;
}
@media screen and (max-width: 768px) {
	.modal-body {
		max-height: 400px;
	}
}
.fade-up-down-enter-active {
	transition: all 0.3s ease;
}
.fade-up-down-leave-active {
	transition: all 0.3s ease;
}
.fade-up-down-enter {
	transform: translateY(10%);
	opacity: 0;
}
.fade-up-down-leave-to {
	transform: translateY(10%);
	opacity: 0;
}

.fade-enter-active {
	-webkit-transition: opacity 2s;
	transition: opacity 0.3s;
}
.fade-leave-active {
	transition: opacity 0.3s;
}

.fade-enter,
.fade-leave-to {
	opacity: 0;
}
</style>
