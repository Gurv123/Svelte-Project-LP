<script>
  import SearchBar from "../../components/searchBar.svelte";
  import Layout from "../__layout.svelte";
  SearchBar
</script>

<Layout>
  <section slot="main" class="wraperSearch">
    <SearchBar />
  </section>
</Layout>