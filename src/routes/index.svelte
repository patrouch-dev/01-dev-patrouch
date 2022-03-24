<svelte:head>
  <title>Welcome</title>

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
	Tip #: {count}
</button>
<p>{count} * 2 = {doubled}</p>
<p>{doubled} * 2 = {quadrupled}</p>

<svelte:body />
<style>
  import css from "./font.css";
  @import url('https://fonts.googleapis.com/css2?family=Hurricane&family=Inspiration&family=Special+Elite&display=swap');
    h1 {
    font-family: 'Special Elite', cursive;

    }
    button {
    font-family: 'Hurricane', cursive; 
	}
    p {
      font-family: 'Special Elite', cursive;
    }
    :global body {
  background-color: lightsteelblue;
  padding: 2%;
}


</style>