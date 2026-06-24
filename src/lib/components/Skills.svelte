<script>
	let { idioma = 'pt' } = $props();
	const textos_skills = {
		pt: {
			linguagens: 'Linguagens de Programação',
			frameworks: 'Frameworks e Bibliotecas',
			persistencia: 'Persistência e Cache',
			ferramentas: 'Ferramentas e Infraestrutura'
		},
		en: {
			linguagens: 'Programming Languages',
			frameworks: 'Frameworks and Libraries',
			persistencia: 'Persistence and Cache',
			ferramentas: 'Tools and Infrastructure'
		},
		de: {
			linguagens: 'Programmiersprachen',
			frameworks: 'Frameworks und Bibliotheken',
			persistencia: 'Datenhaltung und Cache',
			ferramentas: 'Tools & Infrastruktur'
		}
	};
	const minhas_skills = {
		linguagens: ['Go', 'Python', 'Java'],
		frameworks: ['Gin', 'Streamlit'],
		persistencia: ['PostgreSQL', 'SQLite', 'Redis', 'Valkey'],
		ferramentas: ['Docker', 'Neovim', 'Linux', 'Git']
	};
</script>

<!-- 1. O div maior ocupa a tela toda (w-full) com o recuo nas bordas (px-6 md:px-12) -->

<div
	class="w-full px-6 md:px-12 rounded-4xl border border-slate-800 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-x-6 gap-y-10 py-10 bg-slate-950/50"
>
	<div class="flex flex-col">
		<h4 class="text-lg font-bold text-cyan-400 mb-4">{textos_skills[idioma].linguagens}</h4>
		<div class="flex flex-wrap gap-2.5">
			{#each minhas_skills.linguagens as langs}
				<span
					class="hover:scale-105 hover:border-cyan-400 transition-all duration-200 px-3 py-1.5 text-sm bg-slate-900 border border-slate-800 rounded-xl text-slate-300 font-medium transition-all hover:border-slate-700"
				>
					{langs}
				</span>
			{/each}
		</div>
	</div>

	<div class="flex flex-col">
		<!-- Título da Categoria -->
		<h4
			class="hover:scale-105 hover:border-cyan-400 transition-all duration-200 text-lg font-bold text-cyan-400 mb-4"
		>
			{textos_skills[idioma].persistencia}
		</h4>

		<!-- Itens da Categoria -->
		<div class="flex flex-wrap gap-2.5">
			{#each minhas_skills.persistencia as persis}
				<span
					class="hover:scale-105 hover:border-cyan-400 transition-all duration-200 px-3 py-1.5 text-sm bg-slate-900 border border-slate-800 rounded-xl text-slate-300 font-medium transition-all hover:border-slate-700"
				>
					{persis}
				</span>
			{/each}
		</div>
	</div>
	<div class="flex flex-col">
		<h4 class="text-lg font-bold text-cyan-400 mb-4">{textos_skills[idioma].frameworks}</h4>
		<div class="flex flex-wrap gap-2.5">
			{#each minhas_skills.frameworks as framewk}
				<span
					class="hover:scale-105 hover:border-cyan-400 transition-all duration-200 px-3 py-1.5 text-sm bg-slate-900 border border-slate-800 rounded-xl text-slate-300 font-medium transition-all hover:border-slate-700"
				>
					{framewk}
				</span>
			{/each}
		</div>
	</div>
	<div class="flex flex-col">
		<h4 class="text-lg font-bold text-cyan-400 mb-4">{textos_skills[idioma].ferramentas}</h4>
		<div class="flex flex-wrap gap-2.5">
			{#each minhas_skills.ferramentas as ferra}
				<span
					class="hover:scale-105 hover:border-cyan-400 transition-all duration-200 px-3 py-1.5 text-sm bg-slate-900 border border-slate-800 rounded-xl text-slate-300 font-medium transition-all hover:border-slate-700"
				>
					{ferra}
				</span>
			{/each}
		</div>
	</div>
</div>
