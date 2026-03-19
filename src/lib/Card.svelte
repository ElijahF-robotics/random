<script>
    let { number, suit } = $props()

    function getSuit(value) {
        const suits = { heart: "❤️", club: "♣️", diamond: "♦️", spade: "♠️" }
        return suits[value] ?? "♠️"
    }
</script>

<div class="flex flex-col w-32 h-48 bg-white border border-gray-300 rounded-2xl shadow-md p-2">
    <div class="text-xl font-bold">
        {number}
    </div>
    <div class="flex flex-1 items-center justify-center text-4xl">
        {getSuit(suit)}
    </div>
    <div class="text-xl font-bold self-end rotate-180">
        {number}
    </div>
</div>