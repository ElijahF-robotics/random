<script>
   let paraDice6 = $state(0);
   let paraDice20 = $state(0);
   let paraCoin = $state(0);

   function changeDice6() {
       paraDice6 = Math.floor(Math.random() * 6) + 1;
   }

   function changeDice20() {
       paraDice20 = Math.floor(Math.random() * 20) + 1;
   }

   function changeCoin() {
       paraCoin = Math.floor(Math.random() * 2) + 1;
   }
</script>

<div class="grid grid-cols-3 gap-2.5">
    <button onclick={changeDice6}>6 sided die</button>
    <button onclick={changeDice20}>20 sided die</button>
    <button onclick={changeCoin}>Flip coin</button>

    <p>{paraDice6}</p>
    <p>{paraDice20}</p>
    <p>{paraCoin}</p>
</div>