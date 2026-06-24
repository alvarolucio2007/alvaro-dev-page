<script>
	// Definindo os parâmetros de entrada (Props) no Svelte 5
	let { idioma = 'pt' } = $props();
	// Dicionário corrigido e limpo
	const textos = {
		pt: {
			titulo: 'Olá, eu sou o Álvaro!',
			subtitulo: 'Bem-vindo ao meu repertório pessoal.',
			p1: 'Sou desenvolvedor focado em soluções de backend, arquitetura e performance.',
			p2: 'Sinta-se livre para explorar meus links e projetos abaixo.',
			github: 'GitHub pessoal ↗',
			linkedin: 'LinkedIn profissional ↗'
		},
		en: {
			titulo: "Hi, I'm Álvaro!",
			subtitulo: 'Welcome to my personal portfolio.',
			p1: "I'm a developer focused on backend solutions, architecture, and performance.",
			p2: 'Feel free to explore my links and projects below.',
			github: 'Personal GitHub ↗',
			linkedin: 'Professional Linkedin ↗'
		},
		de: {
			titulo: 'Hallöchen, ich bin Álvaro!',
			subtitulo: 'Willkommen bei meinem persönlichen Repertoire.',
			p1: 'Ich bin ein Entwickler, mit Fokus auf Backend-Lösungen, Architektur und Leistung.',
			p2: 'Fühl dich frei, meine Links und Projekte unten zu erkunden.',
			github: 'Persönliches GitHub ↗',
			linkedin: 'Professionelles Linkedin ↗'
		}
	};
</script>

<div class="max-w-2xl mx-auto border border-slate-800 bg-slate-950/50 p-8 rounded-2xl shadow-xl">
	<h1 class="text-4xl font-black mb-2 text-indigo-400">{textos[idioma].titulo}</h1>
	<p class="text-xl text-slate-400 mb-6">{textos[idioma].subtitulo}</p>

	<div class="space-y-4">
		<p class="text-slate-300">{textos[idioma].p1}</p>
		<p class="text-slate-300">{textos[idioma].p2}</p>
	</div>
</div>
