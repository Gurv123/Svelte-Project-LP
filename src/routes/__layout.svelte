<script>
  import Footer from "../components/Footer.svelte";
  import NavBar from "../components/NavBar.svelte";
</script>

<div class="wrapperMain">
  <NavBar />
  <main>
    <slot name="main" />
  </main>
  <Footer />
</div>

<style>
  .wrapperMain {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
    background-color: #b1b1b1;
  }

  main {
    flex-grow: 1;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 2rem;
  }
</style>