<script>
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>
<div class="grid grid-cols-3 gap-0.5">
    <p><a href="/dice">DICE</a></p>
    <p><a href="/cards">CARDS</a></p>
    <p><a href="/">8 BALL</a></p>
</div>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>
{@render children()}
