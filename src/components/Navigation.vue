<template>
  <nav class="navbox">
    <h3 class="navlogo">Logo</h3>
    <div class="navitems">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
  </nav>
  <router-view />
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Navigation",
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.navbox {
  border: 1px solid black;
  height: 80px;
  display: flex;
}
</style>
