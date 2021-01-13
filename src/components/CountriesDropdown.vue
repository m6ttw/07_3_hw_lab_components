<template lang="html">
  <div>
    <!-- <ul>
      <dropdown-component v-for="(country, index) in countries" :country="country" :key="index"></dropdown-component>
    </ul> -->
    <label for="country_select">Select a Country:</label>
    <select id="country_select" v-model="selectedCountry">
      <option disabled value="">Select a country</option>
      <option v-for="country in countries" :value="country">{{country.name}}</option>
    </select>
  </div>

</template>

<script>
import DropdownComponent from './DropdownComponent.vue';

export default {
  name: 'countries-dropdown',
  props: ['countries'],
  components: {
    "dropdown-component": DropdownComponent
  }
}
</script>

<style>

</style>
