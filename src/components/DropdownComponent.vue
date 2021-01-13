<template lang="html">
  <li v-on:change="handleChange">{{country.name}}</li>
</template>

<script>
import { eventBus } from '../main.js';

export default {
  name: 'dropdown-component',
  props: ['country'],
  methods: {
    handleChange(){
      eventBus.$emit('country-selected', this.country)
    }
  }
}
</script>

<style>

</style>
