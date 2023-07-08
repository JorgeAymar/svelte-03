<script>
	let cursos = ['html', 'css', 'js'];
	let numeros = [2, 5, 13];

	const agregarNumero = () => {
		let num = Math.floor(Math.random() * 99 - 1) + 1;
		console.log(num);
		// numeros.push(num);
		numeros = [...numeros, num];
	}
</script>

<main class = "container">
	<h1>Listado de Cursos</h1>
	<ul>
		{#each cursos as curso, index}
			<li>{index + 1 } - {curso}</li>
		{/each}

		<button on:click={agregarNumero} class="btn btn-primary">
			Agregar Número
		</button>

		{#if numeros.length > 5}
			 <h3>Agregaste mas de 5 números!</h3>
		{/if}

		{#each numeros as numero, index}
			<li>{index + 1} - {numero}</li>
		{/each}
	</ul>
</main>

