<script>
  import { onMount } from 'svelte';
  import Layout from './__layout.svelte';

  let countries = [];

  onMount(async () => {
    const response = await fetch('https://restcountries.com/v3.1/all');
    const data = await response.json();
    countries = data;
  })
</script>
  

<Layout>
  <section slot="main" class="wrapperImg">
    {#each countries as country, i}
      <div>
        <a href="/countryDetails?name={country.name.common}"><img src="{country.flags.svg}" alt="{country.name.common}"></a>
      </div>
    {/each}
  </section>
</Layout>


<style>
  .wrapperImg {
    display: flex;

    gap: 2rem;
    flex-wrap: wrap;
    justify-content: center;
  }

  img {
    width: 150px;
    max-height: 100px;
  }
</style>