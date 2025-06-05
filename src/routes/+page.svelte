<script>
  import Header from "$lib/Header.svelte"
  import ImageCard from "$lib/ImageCard.svelte"
  let name = "world"
  let imageUrl = "https://picsum.photos/200"
  let isChecked = false
  let selectedOption = "Option 1"
  let count = 0
  function increment() {
    count = count + 1
  }
  function decrement() {
    count = count - 1
  }
</script>

<Header />

<main class="content section">
  <input bind:value={name} placeholder="Enter your name" />
  <h1>Hello {name}!</h1>

  <input type="checkbox" bind:checked={isChecked} />
  <p>The checkbox is {isChecked}.</p>

  <select bind:value={selectedOption}>
    <option value="Option 1">Option 1</option>
    <option value="Option 2">Option 2</option>
    <option value="Option 3">Option 3</option>
  </select>
  <p>You selected: {selectedOption}</p>

  <p>Count: {count}</p>
  <button on:click={increment}>Increment</button>
  <button on:click={decrement}>Decrement</button>
  <img src={imageUrl} alt="Example" />
  <ImageCard />
</main>

<footer class="footer">
  <p class="has-text-centered">&copy; Craighead Diocesan School 2025</p>
</footer>
