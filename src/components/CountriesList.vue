<template lang="html">
  <div>
    <!-- <ul>
      <list-component v-for="(country, index) in countries" :country="country" :key="index"></list-component>
    </ul> -->
    <label for="country_select">Select a Country:</label>
    <select id="country_select" v-model="selectedCountry">
        <option disabled value="">Select a country</option>
        <option v-for="(country, index) in countries" :country="country" :key="index">{{country.name}}</option>
    </select>
  </div>

</template>

<script>
import ListComponent from './ListComponent.vue';

export default {
  name: 'countries-list',
  props: ['countries'],
  components: {
    "list-component": ListComponent
  }
}
</script>

<style>

</style>
