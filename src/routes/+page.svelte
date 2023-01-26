<script>
  import NavBar from "../components/navBar.svelte";
  import Footer from "../components/footer.svelte";
  import Main from "../components/main.svelte";
</script>

<div class="wrapperMain">
  <NavBar />
  <Main />
  <Footer />
</div>

<style>
  .wrapperMain {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }
</style>