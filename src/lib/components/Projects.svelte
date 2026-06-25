<script>
	let { idioma = 'pt' } = $props();
	const titulos_projetos = {
		link_shortener: 'Encurtador de Links',
		py_go_lib: 'PyGoLib',
		sapiens_go: 'SapiensGo'
	};
	const links_github = {
		link_shortener: 'https://github.com/alvarolucio2007/encurtador-links-go',
		py_go_lib: 'https://github.com/alvarolucio2007/PyGoLib',
		sapiens_go: 'https://github.com/alvarolucio2007/SapiensGo'
	};
	const textos_projetos = {
		pt: {
			link_shortener:
				'Microsserviço de encurtamento de URLs focado em baixa latência, containerizado com Docker e otimizado para ambientes de nuvem.',
			py_go_lib:
				'Sistema fullstack de livraria baseado em uma API REST estritamente tipaga em Go, utilizando o framework Gin e persistência relacional com PostgreSQL.',
			sapiens_go:
				'Serviço escolar de alta performance, baseado em APIs gRPC, REST e otimização de leitura a partir de Cache Redis assíncrono.'
		},
		en: {
			link_shortener:
				'URL shortening microservice, focused on low latency, containerized with Docker and optimized for cloud-based environments.',
			py_go_lib:
				'Fullstack library system based on strictly typed RESTful APIs in Go, utilizing the Gin framework with relational persistence from PostgreSQL.',
			sapiens_go:
				'Highly performant school service, based on gRPC and RESTful APIs, and reading optimizations based on an asynchronous Redis cache.'
		},
		de: {
			link_shortener:
				'URL-Shortener-Mikroservice mit Fokus auf niedrige Latenz, containerisiert mit Docker und optimiert für Cloud-Umgebungen.',
			py_go_lib:
				'Fullstack-Bibliothekssystem basierend auf streng typisierten RESTful APIs in Go, unter Verwendung des Gin-Frameworks mit relationaler Persistenz in PostgreSQL.',
			sapiens_go:
				'Hochleistungsfähiger Schulservice basierend auf gRPC- und RESTful-APIs, inklusive Leseoptimierung durch asynchronen Redis-Cache.'
		}
	};
	const stack_projetos = {
		link_shortener: ['Go', 'PostgreSQL', 'Redis', 'Docker'],
		py_go_lib: ['Go', 'Gin', 'Python', 'Streamlit', 'Docker', 'PostgreSQL'],
		sapiens_go: ['Go', 'Gin', 'Python', 'Streamlit', 'Docker', 'PostgreSQL', 'Redis', 'gRPC']
	};
</script>

<div
	class="w-full px-6 md:px-12 rounded-4xl border border-slate-800 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-x-6 gap-y-10 py-10 bg-slate-950/50"
>
	{#each Object.keys(textos_projetos[idioma]) as id_projeto}
		<div
			class="flex flex-col justify-between h-full p-4 border border-slate-900 rounded-2xl bg-slate-950/30"
		>
			<div>
				<div class="flex justify-between items-center mb-3">
					<h4 class="text-xl font-bold text-cyan-400">
						{titulos_projetos[id_projeto]}
					</h4>
					<a
						href={links_github[id_projeto]}
						target="_blank"
						rel="noopener noreferrer"
						class="text-xs text-slate-500 hover:text-cyan-400 transition-colors duration-200 font-medium whitespace-nowrap"
					>
						Ver projeto →
					</a>
				</div>

				<p class="text-sm text-slate-300 px-3 py-4 mb-4 leading-relaxed">
					{textos_projetos[idioma][id_projeto]}
				</p>
			</div>

			<div class="flex flex-wrap gap-1.5 mt-auto gap-2">
				{#each stack_projetos[id_projeto] as tech}
					<span
						class="px-2 py-0.5 text-xs bg-slate-900 border border-slate-700 rounded-md text-slate-400"
					>
						{tech}
					</span>
				{/each}
			</div>
		</div>
	{/each}
</div>
