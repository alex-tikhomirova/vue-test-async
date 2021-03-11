<template>
  <div>
    <teleport to="#header">
     <Header v-if="show"></Header>
    </teleport>
    <button v-on:click="show = true">x</button>
    {{ text }}
  </div>
</template>

<script>
//import Header from "./components/header/Header.vue";
import {defineAsyncComponent} from "vue";

export default {
  name: "App",
  components: {
  // Header,
       // Header:() => import("./components/header/Header.vue")
    Header: defineAsyncComponent(() =>
        import('./components/header/Header.vue')
    )

  },
  data(){
    return {
      text: 'vue app',
      show: false,
    }
  }
}
</script>

<style scoped>

</style>