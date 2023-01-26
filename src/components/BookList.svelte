<script>
  export let books = [];
</script>

<div class="books">
  {#each books as book}
    <div class="book">
      <img src={book.coverUrl} alt={book.title} />
      <div>
        <h2>{book.title}</h2>
        <p>{book.author}</p>
      </div>
    </div>
  {/each}
</div>

<style>
  .books {
    display: flex;
    flex-wrap: wrap;
  }

  .book {
    flex: 1 1 300px;
    margin: 10px;
  }

  .book img {
    max-width: 100%;
  }
</style>