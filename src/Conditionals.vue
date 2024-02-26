<template>
  <h2 v-if="num === 0">This is zero</h2>
  <h2 v-else-if="num < 0">This is negative</h2>
  <h2 v-else-if="num > 0">This is positive</h2>
  <h2 v-else>This is not a number</h2>
  <h2 v-show="isVisible">Data is visible</h2>

  <template v-if="fruitsVisible">
    <h2>Apple</h2>
    <h2>Banana</h2>
    <h2>Mango</h2>
  </template>
</template>

<script>
  import { resolveDirective } from 'vue';
import App from './Conditionals.vue';

  export default {
    name: App,
    data() {
      return{
        num: 0,
        isVisible: false,
        fruitsVisible: false
      }
    }
  }
</script>

<style>
  #app {

  }
</style>