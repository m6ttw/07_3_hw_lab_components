<template>
  <div>
    <h1>Countries</h1>
    <div class="main-container">
      <countries-dropdown :countries='countries'></countries-dropdown>
      <country-detail :country='selectedCountry'></country-detail>
    </div>
  </div>
</template>

<script>
import CountriesDropdown from './components/CountriesDropdown.vue';
import CountryDetail from './components/CountryDetail.vue';
import { eventBus } from './main.js';

export default {
  name: "app",
  data(){
    return {
      countries: [],
      selectedCountry: null
    }
  },
  mounted(){
    fetch("https://restcountries.eu/rest/v2/all")
    .then(res => res.json())
    .then(countries => this.countries = countries)

    eventBus.$on('country-selected', (country) => {
      this.selectedCountry = country
    })
  },
  components: {
    "countries-dropdown": CountriesDropdown,
    "country-detail": CountryDetail
  }
}
</script>

<style>

</style>
