<template>
  <div class="header">
    <Menu></Menu>
    <Cart></Cart>
  </div>
</template>

<script>
import Menu from "./Menu.vue";
import Cart from "./Cart.vue";
export default {
  name: "Header",
  components: {Cart, Menu}
}
</script>

<style scoped>

</style>