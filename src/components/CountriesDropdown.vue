<template lang="html">
  <div>
    <!-- <ul>
      <dropdown-component v-for="(country, index) in countries" :country="country" :key="index"></dropdown-component>
    </ul> -->
      <label for="country_select">Select a Country:</label>
      <select dropdown-component>
        <option disabled value="">Select a country</option>
        <option v-for="(country, index) in countries" :country="country" :key="index">{{country.name}}</option>
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
