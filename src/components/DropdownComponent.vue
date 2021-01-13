<template lang="html">
  <li v-on:change="handleClick">{{country.name}}</li>
</template>

<script>
import { eventBus } from '../main.js';

export default {
  name: 'dropdown-component',
  props: ['country'],
  methods: {
    handleClick(){
      eventBus.$emit('country-selected', this.country)
    }
  }
}
</script>

<style>

</style>
