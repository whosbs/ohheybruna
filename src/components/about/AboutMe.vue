<script>
export default {
	setup() {
		return {
			bios: [
				{
					id: 1,
					bio:
						'Sou uma alma criativa e curiosa, que encontrou no design uma maneira de levar a vida exercitanto sempre as aréas que mais me interessam e estimulam. Estou sempre em busca de novas inspirações e antenada nas trends, tudo para produzir um conteúdo com mais valor e evoluir como profissional.',
				},
				{
					id: 2,
					bio:
						'Encontrei no Design uma forma de continuar a ser curiosa, descobrindo coisas novas e de certa forma fazendo arte. Mas, principalmente, o Design me possibilita utilizar uma das minhas ‘skills’ mais poderosas, a empatia. Com o passar dos anos, a gente vai aprendendo a ser mais dura, mas ver o lado bom das pessoas e entender o que se passa nelas, é essencial não só para o lado profissional, mas principalmente humano.',
				},

								{
					id: 3,
					bio:
						'Cada vez mais, sei que meu trabalho vai muito além do visual: se trata de transmitir essências, uma mensagem para ser contada junto com boas histórias!',
				},
			],
		};
	},
};
</script>

<template>
	<div class="block sm:flex sm:gap-10 mt-10 sm:mt-20">
		<!-- About profile image -->
		<div class="w-full sm:w-1/4 mb-7 sm:mb-0">
			<img
				src="@/assets/images/profile.jpeg"
				class="rounded-xl w-96"
				alt=""
			/>
		</div>

		<!-- About details -->
		<div class="w-full sm:w-3/4 text-left">
			<p
				v-for="bio in bios"
				:key="bio.id"
				class="font-general-regular mb-4 text-ternary-dark dark:text-ternary-light text-lg"
			>
				{{ bio.bio }}
			</p>
		</div>
	</div>
</template>
