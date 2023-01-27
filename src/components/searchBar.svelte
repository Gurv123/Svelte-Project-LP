<script>
  let btnSearch = document.getElementById('btn-search');
  let countryName = 'undefined';

  function click() {
    if (document.getElementById('searchBar').value != null) {
      countryName = document.getElementById('searchBar').value;
    }
  }
</script>

<h2>Search a country</h2>

<section class="container">
  <input type="text" name="search"  class="searchBar" id="searchBar"/>
  <a href="/countryDetails?name={countryName}">
    <button class="btn-search" id="btn-search" on:click={click}>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 24 24"
        width="24"
        height="24"
        ><path fill="none" d="M0 0h24v24H0z" /><path
          d="M18.031 16.617l4.283 4.282-1.415 1.415-4.282-4.283A8.96 8.96 0 0 1 11 20c-4.968 0-9-4.032-9-9s4.032-9 9-9 9 4.032 9 9a8.96 8.96 0 0 1-1.969 5.617zm-2.006-.742A6.977 6.977 0 0 0 18 11c0-3.868-3.133-7-7-7-3.868 0-7 3.132-7 7 0 3.867 3.132 7 7 7a6.977 6.977 0 0 0 4.875-1.975l.15-.15z"
        /></svg
      >
    </button>
  </a>
</section>

<style>
  h2 {
    text-align: center;
    margin: 4rem;
  }

  .container {
    background-color: rgba(4, 59, 92, 0.5);
    max-width: 764px;
    width: 30rem;
    height: 4rem;
    padding: 1rem;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 10rem;
  }
  .btn-search {
    background-color: transparent;
    border: none;
  }

  .searchBar {
    background-color: transparent;
    color: #000;
    border: none;
    height: 85%;
    width: 100%;
    padding: 0.5rem;
  }

  .searchBar:focus {
    outline: none;
  }
</style>
