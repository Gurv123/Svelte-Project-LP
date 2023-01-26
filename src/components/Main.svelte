<script>
  import BookList from './BookList.svelte';
  let books = [
    {
      title: "Harry Potter and the Sorcerer's Stone",
      author: "J.K. Rowling",
      coverUrl: "https://images.example.com/hp1.jpg"
    },
    {
      title: "The Hunger Games",
      author: "Suzanne Collins",
      coverUrl: "https://images.example.com/hungergames.jpg"
    },
    //...
  ]
</script>

<main>
  <BookList this={books} />
</main>

<style>
  main {
    flex-grow: 1;
  }
</style>