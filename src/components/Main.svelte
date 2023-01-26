<script>
import BookList from './BookList.svelte';
  let books = [
    {
      title: "Harry Potter and the Sorcerer's Stone",
      author: "J.K. Rowling",
    },
    {
      title: "The Hunger Games",
      author: "Suzanne Collins",
    },
  ]
</script>

<main>
  <BookList {books} />
</main>

<style>
  main {
    flex-grow: 1;
  }
</style>