<script>
  import { onMount } from 'svelte';
  import Layout from "../__layout.svelte";

  let params = (new URL(document.location)).searchParams;
  let nameCountry = params.get('name');

  let countries = [];
  let urlFetch;

  onMount(async () => {
    urlFetch = "https://restcountries.com/v3.1/name/"+nameCountry;
    const response = await fetch(urlFetch);
    const data = await response.json();
    countries = data;
  })
</script>

<Layout>
  <section slot="main" class="wraperCountryDetails">
    {#each countries as country}

      <h2><strong>{country.name.common}</strong></h2>

      <div class="wrapperInfos">
        <section class="wraperImg">
          <img src="{country.flags.svg}" alt="Drapeau {country.name.common}"/>
        </section>
        
        <section class="wrapperDetails">
          <p><strong>Official name :</strong> {country.name.official}</p>
          <p><strong>Capital :</strong> {country.capital}</p>
          <p><strong>Continent :</strong> {country.region}</p>
          <p><strong>Population :</strong> {country.population}</p>
          {#if country.independent == "true"}
            <p><strong>Independent :</strong> Yes</p>
          {:else}
            <p><strong>Independent :</strong> No</p>
          {/if}
          <p><strong>Top-level domain :</strong> {country.tld}</p>
        </section>
      </div>
    {/each}
  </section>
</Layout>

<style>
  .wraperCountryDetails {
    display: flex;
    flex-direction: column;
  }

  .wraperCountryDetails h2 {
    text-align: center;
    margin-bottom: 4rem;
  }

  .wrapperInfos {
    display: flex;
    justify-content: space-around;
    align-items: center;
  }

  .wraperCountryDetails .wraperImg {
    padding: 1rem;
    width: 50%;
  }

  .wraperCountryDetails .wraperImg img {
    width: 100%;
  }

  .wraperCountryDetails .wrapperDetails p {
    padding: 0.5rem;
  }
</style>