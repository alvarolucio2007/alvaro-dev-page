<script>
	let { idioma = 'pt' } = $props();
	const textos_hero = {
		pt: {
			motto: 'Álvaro | Engenheiro de software de 18 anos do Brasil 🇧🇷',
			resumo:
				'Desenvolvedor backend focado em Go, bancos de dados relacionais e não relacionais. Transformo ideias em produtos concretos e performáticos.',
			cta_github: 'Visite meu GitHub',
			cta_curriculo: 'Ver Currículo',
			cta_contato: 'Contato'
		},
		en: {
			motto: 'Álvaro | 18 year old Software Engineer from Brazil 🇧🇷',
			resumo:
				'Backend developer focused on Go, relational and non-relational databases. I transform ideas into concrete and performant products.',
			cta_github: 'Visit my GitHub',
			cta_curriculo: 'See my Resume',
			cta_contato: 'Contact'
		},
		de: {
			motto: 'Álvaro | 18-jähriger alt Softwareingeniur aus Brasilien 🇧🇷',
			resumo:
				'Backend-Entwickler mit Fokus auf Go, relationale und nicht-relationale Datenbanken. Ich verwandle Ideen in greifbare und leistungsstarke Produkten',
			cta_github: 'GitHub besuchen',
			cta_curriculo: 'Lebenslauf ansehen',
			cta_contato: 'Kontakt aufnehmen'
		}
	};
</script>

<!-- 1. Adicionamos 'flex flex-col justify-between h-full' na div principal do Hero -->
<div
	class="max-w-4xl mr-auto border border-slate-800 bg-slate-950/50 p-8 rounded-4xl shadow-xl flex flex-col justify-between h-full"
>
	<!-- 2. Envolvemos os textos superiores em uma div para que eles fiquem juntos no topo -->
	<div>
		<h1 class="text-4xl font-black mb-2 text-cyan-300">{textos_hero[idioma].motto}</h1>
		<h2 class="text-2xl text-slate-300 mb-6">{textos_hero[idioma].resumo}</h2>
	</div>

	<!-- 3. A div dos botões agora vai ser empurrada automaticamente para o final de tudo -->
	<div class="flex flex-wrap gap-4 mt-2">
		<a
			href="https://github.com/alvarolucio2007"
			target="_blank"
			rel="noopener noreferrer"
			class="px-5 py-2.5 bg-cyan-600 hover:bg-cyan-500 text-slate-950 font-bold rounded-xl transition-all duration-200 shadow-lg shadow-cyan-600/10 text-sm"
		>
			{textos_hero[idioma].cta_github}
		</a>

		<!-- Botão Secundário: Currículo -->
		<a
			href="https://drive.proton.me/urls/1R9JRYCA2W#0Sl28poz08zx"
			target="_blank"
			class="px-5 py-2.5 bg-slate-950 hover:bg-cyan-950/30 text-cyan-400 font-bold rounded-xl border border-cyan-700/50 transition-all duration-200 text-sm"
		>
			{textos_hero[idioma].cta_curriculo}
		</a>
	</div>
</div>
