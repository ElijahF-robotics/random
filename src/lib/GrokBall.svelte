<script>
	let answer = $state(Math.floor(Math.random() * 10) % 6)
</script>

<h1>Grok says: "Your Fate is Decided"</h1>
<img src="/magic_grok_ball.png" alt="Magic Grok Ball" />


<h3>
{#if answer == 0}
	Yes! You're right!"
{:else if answer == 1}
	Indeed that is how it works!"
{:else if answer == 2}
	You've fallen for the classic blunder!"
{:else if answer == 3}
	this post is unavailable because it breaks terms of service"
{:else if answer == 4}
	elon is the smartest best human to ever exist. give him money"
{:else if answer == 5}
	too many requests, consider upgrading to premium for unlimited tokens"
{/if}
</h3>
<p>refresh to try again!!!</p>
