<script>
	import Hero from '$lib/components/Hero.svelte';
	import AboutMe from '../lib/components/AboutMe.svelte';
	import Name from '../lib/components/Name.svelte';
	let idioma = $state('pt');

	// Array de suporte para renderizar os botões dinamicamente
	const botoesIdioma = [
		{ id: 'pt', label: '🇧🇷 PT' },
		{ id: 'en', label: '🇺🇸 EN' },
		{ id: 'de', label: '🇩🇪 DE' }
	];
</script>

<main class="min-h-screen bg-slate-900 text-slate-100 font-sans p-6">
	<div class="max-w-5xl ml-auto flex justify-end gap-3 mb-8">
		{#each botoesIdioma as botao}
			<button
				onclick={() => (idioma = botao.id)}
				class="px-3 py-1 rounded text-sm font-bold transition {idioma === botao.id
					? 'bg-indigo-600 text-white'
					: 'bg-slate-800 text-slate-400 hover:bg-slate-700'}"
			>
				{botao.label}
			</button>
		{/each}
	</div>
	<Name {idioma} />
	<div class="grid grid-cols-1 md:grid-cols-2 gap-12">
		<!-- Div da Esquerda (Hero) -->
		<Hero {idioma} />
		<!-- Div da Direita (About Me) -->
		<AboutMe {idioma} />
	</div>
</main>
