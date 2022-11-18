<template>
  <div id="app">
    <navbarrr @toggleText="change"/>
    <start :showingLB="showingLB"/>

  </div>
</template>

<script>
import navbarrr from "./components/navbar.vue"
import start from "./components/start.vue"
import home from "./components/home.vue"

export default {
  name: 'App',
  components: {
    navbarrr,
    start,
    home
  },
  data() {
    return {
      showingLB: true
    }
  },
  methods: {
    change(){
      this.showingLB = !this.showingLB
      console.log("Hola PApito");
    }
  },
}
</script>

<style>
#app {
  margin: 0;
  padding: 0;
}

</style>
