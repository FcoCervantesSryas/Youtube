<template>
    <div class="start">
        <leftBar v-if="showingLB"/>
        <leftBar2 v-if="!showingLB"/>
        <home/>
    </div>
</template>

<script>
import leftBar from "./leftBar.vue";
import leftBar2 from "./leftBar2.vue";
import home from "./home.vue"

export default {
  name: 'start',
  components:{
    leftBar,
    leftBar2,
    home
  },
  props:{
    showingLB:{
      type: Boolean
    }
  }
}
</script>

<style scoped>
.start{
    height: calc(100vh - 56px);
    display: flex;
    margin: 0%;
    padding: 0;
}

</style>