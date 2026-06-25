<script>
	let { idioma = 'pt' } = $props();
	const titulo_contato = {
		pt: 'Vamos transformar ideias em software de verdade!',
		en: `Let's transform ideas into real software!`,
		de: `Lassen Sie uns Ideen zum echten Software verwandeln!`
	};
	const header_contato = {
		pt: 'Em busca de oportunidades de estágio e projetos desafiadores. Se quiser trocar uma ideia sobre desenvolvimento de software, containerização, ou precisa de ajuda com algum projeto, só chamar!',
		en: 'Looking for internship opportunities and challenging projects. If you want to chat about software development, containerization or need help with a project, feel free to reach out!',
		de: 'Auf der Suche nach Praktika und herausfordernden Projekten. Wenn Sie sich über Softwareentwicklung oder Containerisierung austauschen möchten oder Hilfe bei einem Projekt brauchen, melden Sie sich einfach!'
	};
	const contacts = [
		{ nome: 'GitHub', user: 'alvarolucio2007', url: `https://github.com/alvarolucio2007` },
		{ nome: 'LinkedIn', user: 'alvarolucio', url: `https://linkedin.com/in/alvarolucio` },
		{ nome: 'E-mail', user: 'alvarolucio2007@gmail.com', url: `mailto:alvarolucio2007@gmail.com` }
	];
</script>

<div
	class="w-full px-6 md:px-12 rounded-4xl border border-slate-800 grid grid-cols-1 md:grid-cols-2 gap-x-12 gap-y-10 py-10 bg-slate-950/50"
>
	<div class="flex flex-col justify-center">
		<h1 class="text-3xl font-black mb-2 text-cyan-400">{titulo_contato[idioma]}</h1>
		<h2 class="text-xl text-slate-300 leading-relaxed">{header_contato[idioma]}</h2>
	</div>

	<div class="flex flex-col justify-center gap-4">
		{#each contacts as contato}
			<a
				href={contato.url}
				target="_blank"
				rel="noopener noreferrer"
				class="flex items-center justify-between p-4 rounded-xl border border-slate-900 bg-slate-950/30 hover:border-cyan-400/50 hover:bg-slate-900/40 hover:scale-[1.02] transition-all duration-300 group"
			>
				<div class="flex items-center gap-3">
					<span
						class="text-sm font-semibold text-slate-200 group-hover:text-indigo-400 transition-colors"
					>
						{contato.nome}
					</span>
					<span class="text-xs text-slate-500">
						{contato.user}
					</span>
				</div>
				<span class="text-xs text-slate-600 group-hover:text-cyan-400 transition-colors">↗</span>
			</a>
		{/each}
	</div>
</div>
