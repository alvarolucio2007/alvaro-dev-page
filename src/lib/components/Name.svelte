<script>
	let { idioma = 'pt' } = $props();
	const textos_nome = {
		pt: { titulo: 'Olá, eu sou o Álvaro!' },
		en: { titulo: "Hi, I'm Álvaro!" },
		de: { titulo: 'Hallo, mein Name ist Álvaro!' }
	};

	let textoExibido = $state('');

	// O Svelte 5 monitora automaticamente qualquer estado lido dentro do $effect
	$effect(() => {
		// Ao ler 'idioma' e 'textos_about_me' aqui, o Svelte sabe que deve reiniciar o efeito quando eles mudarem
		const textoCompleto = textos_nome[idioma].titulo;

		textoExibido = '';
		let index = 0;
		let intervalo;

		// Função que digita caractere por caractere
		intervalo = setInterval(() => {
			if (index < textoCompleto.length) {
				textoExibido = textoCompleto.slice(0, index + 1);
				index++;
			} else {
				clearInterval(intervalo);
			}
		}, 70); // 70ms fica uma velocidade bem natural de digitação

		// Cleanup: Se o idioma mudar no meio da digitação, limpa o timer anterior
		return () => clearInterval(intervalo);
	});
</script>

<h1 class="text-4xl font-black mb-8 text-indigo-400 text-center min-h-[40px]">
	{textoExibido}<span class="animate-pulse text-indigo-500">|</span>
</h1>
