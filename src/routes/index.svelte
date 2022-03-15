<svelte:head>
    <link href="https://fonts.googleapis.com/css?family=Gelasio" rel="stylesheet">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Changa">

</svelte:head>
<h1>cleva</h1>
<script>
	let count = 1;

	// the `$:` means 're-run whenever these values change'
	$: doubled = count * 2;
	$: quadrupled = doubled * 2;

	function handleClick() {
		count += 1;
	}
</script>
<button on:click={handleClick}>
	Cleva Tip #: {count}
</button>
<p>{count} * 2 = {doubled}</p>
<p>{doubled} * 2 = {quadrupled}</p>

<svelte:body />
<style>
    @font-face {
        font-family: 'Gelasio';
        font-style: normal;
        font-weight: 400;
        src: local('Gelasio Regular'), local('Gelasio-Regular'), url(https://fonts.gstatic.com/s/gelasio/v1/cIf9MaFfvUQxTTqS9C6hYQ.woff2) format('woff2');
        unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
    }

    h1 {
        font-family: Gelasio

    }
    button {
		font-family: "Changa", sans-serif;
	}
    p {
    font-family: "Changa", sans-serif;
    }
    :global body {
  background-color: orangered;
  padding: 2%;
}


</style>