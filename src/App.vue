<template>  
  <p>{{greeting}} {{name}}</p>
  <button @click="name='Pablo'">Change name</button>
  <p v-text="question"></p>
  <p v-html="htmlData" :id="id" :class="id" :style="style"></p>

  <!-- Counter app -->
  <h2>{{ count }}</h2>
  <button @click="increment(1)">Add +1 </button>
  <button @click="decrement(2)">Sub -2</button>
</template>

<script>
import { resolveDirective } from 'vue';


export default {
  name: 'App',
  data() {
    return {
      name: 'Javi',
      count: 0,
      greeting: 'Hola',
      question: '¿Cómo estás?',
      htmlData: '<b>Soy un bloque de HTML</b>',
      id: 'new',
      style: {
        color: 'red',
        backgroundColor: 'black'
      }      
    }
  },
  methods: {
        increment(num) {
          this.count += num
        },
        decrement(num) {
          this.count -=num
        }
      }
}
</script>

<style>
#app {
  
}
</style>
