<template>
  <GreetVue name="Sam"/>
  <GreetVue name="Mike"/>
  <GreetVue :name="name" /> <!--  v.bind:name = :name porque trae el data del model -->

  <!-- Emitter Example -->

  <button @click="isPopupVisible = true">Show Popup</button>
  <PopupVue v-if="isPopupVisible" @close="isPopupVisible=false"/>

  <!-- Slots example -->

  <CardVue>This is our first slot</CardVue>
  <CardVue><h1>This is our first slot</h1></CardVue>
  <CardVue><img src="https://placehold.co/300x200"/></CardVue>

</template>

<script>
import GreetVue from './components/Greet.vue';
import PopupVue from './components/Popup.vue';
import CardVue from './components/Card.vue';
export default {
  name: 'AppWithComponents',
  components:{
    GreetVue,
    PopupVue,
    CardVue
  },
  data() {
    return {
      name: 'Superman',
      isPopupVisible: false
    }
  }
}
</script>

<style>
  #app {

  }
</style>
