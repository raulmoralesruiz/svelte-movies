<script>
	export let initialCounter = 0;
	let contador = initialCounter;
  export let maxCounter = 9;

	function handleClick() {
		contador++
	}

  $: isEvenOrOdd = contador % 2 === 0 ? 'Is even' : 'Is odd'
  $: if (contador > maxCounter) {
      console.log('limit contador');
      contador = maxCounter
    }
  
</script>

<main>
	<button on:click="{handleClick}">Incrementar</button>
	<span>{contador}</span>
  <span>{isEvenOrOdd}</span>

	<!-- <p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p> -->
</main>

<style>
	/* main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	} */

	span {
		color: #ff3e00;
		/* text-transform: uppercase;
		font-size: 4em;
		font-weight: 100; */
	}

	/* @media (min-width: 640px) {
		main {
			max-width: none;
		}
	} */
</style>