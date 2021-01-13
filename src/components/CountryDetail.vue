<template lang="html">
  <div v-if='country'>
    <h3>{{country.name}}</h3>
    <p>Capital: {{country.capital}}</p>
    <p>Subregion: {{country.subregion}}</p>
    <p>Population: {{country.population}}</p>
  </div>
</template>

<script>
import { eventBus } from '../main.js';

export default {
  name: 'country-detail',
  props: ['country']
}

</script>

<style>

</style>
