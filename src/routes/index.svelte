<svelte:head>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Changa">
    <link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Hurricane&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Hurricane&family=Inspiration&display=swap" rel="stylesheet">
<link rel="preload" href="https://fonts.gstatic.com/s/quicksand/v7/6xKtdSZaM9iE8KbpRA_hK1QNYuDyPw.woff2" as="font" crossorigin>
<link rel="preload" href="https://fonts.gstatic.com/s/lato/v14/S6uyw4BMUTPHjx4wXiWtFCc.woff2" as="font" crossorigin>


</svelte:head>
<h1>Christopher Patrouch</h1>
<p>Traction Developer, alpha testing</p>
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
 font-family: 'Lato';
 font-style: normal;
 font-weight: 400;
 src: local('Lato Regular'), local('Lato-Regular'), url(https://fonts.gstatic.com/s/lato/v14/S6uyw4BMUTPHjx4wXiWtFCc.woff2) format('woff2');
 unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
}
@font-face {
 font-family: 'Quicksand';
 font-style: normal;
 font-weight: 400;
 src: local('Quicksand Regular'), local('Quicksand-Regular'), url(https://fonts.gstatic.com/s/quicksand/v7/6xKtdSZaM9iE8KbpRA_hK1QNYuDyPw.woff2) format('woff2');
 unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
}
    h1 {
        font-family: 'Lato', cursive;

    }
    button {
		font-family: "Quicksand", cursive;
	}
    p {
    font-family: 'Hurricane', cursive; 
    }
    :global body {
  background-color: lightblue;
  padding: 2%;
}


</style>