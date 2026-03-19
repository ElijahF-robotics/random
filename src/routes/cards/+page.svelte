<script>
    import Card from "$lib/Card.svelte";
    import './layout.css';

    let cards = $state([])

    const SUITS = ["heart", "club", "diamond", "spade"]
    const VALUES = ["A", "2", "3", "4", "5", "6", "7", "8", "9", "10", "J", "Q", "K"]

    function pickCards(n = 5) {
        const deck = SUITS.flatMap(suit => VALUES.map(value => ({ number: value, suit })))
        cards = deck.sort(() => Math.random() - 0.5).slice(0, n)
    }

</script>

<div class="flex flex-col w-screen h-screen bg-gray-200 items-center justify-center gap-6">
    <h1 class="text-3xl font-bold">Pick some cards!</h1>
    <button
            class="px-4 py-2 bg-blue-200 hover:bg-blue-400 text-white font-semibold rounded-xl shadow"
            onclick={() => pickCards()}
    >
        Pick the cards
    </button>
    <div class="flex flex-row flex-wrap justify-center gap-3">
        {#each cards as card}
            <Card number={card.number} suit={card.suit} />
        {/each}
    </div>
</div>