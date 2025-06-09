<script>
  let NZD = 0
  let fromCurrency = "USD"
  let toCurrency = "NZD"
  function convertCurrency() {
    NZD = NZD * 1.66
  }
</script>

<p>Convert {fromCurrency} to {toCurrency}</p>

<input bind:value={NZD} placeholder="Enter amount" />
<button on:click={convertCurrency}>Convert to NZD</button>

<style>
  input {
    width: 10rem;
    height: 2rem;
    margin: 1rem;
    padding: 0.5rem;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
</style>
