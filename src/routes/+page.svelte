<script>
  import NavBar from "../components/NavBar.svelte";
  import Footer from "../components/Footer.svelte";
  import Main from "../components/Main.svelte";
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