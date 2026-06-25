<script lang="ts">
	let { idioma = 'pt' } = $props();

	const textos_about_me = {
		pt: {
			titulo: 'Sobre Mim',
			bio: 'Sou estudante de Engenharia de Software com uma profunda paixão pelo desenvolvimento backend. Meu dia a dia gira em torno de escrever código limpo e entender arquiteturas de sistemas. Além da minha especialização em Go, tenho familiaridade com ambientes Linux/Unix devido ao meu uso diário. Gosto de quebrar a cabeça com problemas lógicos e transformá-los em produtos performáticos.'
		},
		en: {
			titulo: 'About Me',
			bio: 'I am a Software Engineering student with a deep passion for backend development. My day-to-day routine revolves around writing clean code and understanding system architectures. In addition to specializing in Go, I am comfortable working in Linux/Unix environments due to my daily use. I love analyzing complex logical problems and transforming them into high-performance products.'
		},
		de: {
			titulo: 'Über mich',
			bio: 'Ich bin Software-Engineering-Student mit einer tiefen Leidenschaft für die Backend-Entwicklung. Mein Alltag dreht sich um das Schreiben von sauberem Code und das Verstehen von Systemarchitekturen. Neben meiner Spezialisierung auf Go bewege ich mich aufgrund meiner täglichen Nutzung sicher in Linux/Unix-Umgebungen. Ich liebe es, komplexe logische Probleme zu analysieren und sie in performante Produkte zu verwandeln.'
		}
	};
</script>

<div class="max-w-4xl ml-auto border border-slate-800 bg-slate-950/50 p-8 rounded-4xl shadow-xl">
	<!-- Título do Card separado do texto -->
	<h3 class="text-2xl font-black mb-4 text-cyan-400">
		{textos_about_me[idioma].titulo}
	</h3>

	<!-- Texto da bio formatado corretamente para leitura -->
	<p class="font-sans text-xl text-gray-200 leading-relaxed">
		{textos_about_me[idioma].bio}
	</p>
</div>
