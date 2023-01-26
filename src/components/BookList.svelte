<script>
  export let books;
</script>

<div class="books">
  {#each books as book}
    <div class="book">
      <div>
        <h2>{book.title}</h2>
        <p>{book.author}</p>
      </div>
    </div>
  {/each}
</div>

<style>
  .books {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    gap: 10px;
  }

  .book {
    border: 1px solid #000;
  }
</style>