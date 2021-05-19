<template>
  <nav class="navbox">
    <h3 class="navlogo">Logo</h3>
    <div class="navitems">
      <router-link to="/">Home</router-link>
      <router-link to="/projects">Projects</router-link>
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
  background: rgb(64, 11, 71);
  height: 80px;
  display: flex;
  align-items: center;
  justify-content: space-around;

  .navitems {
    border: 1px solid pink;
    font-size: 1.2em;
    padding: 10px;
    a {
      text-decoration: none;
      margin: 10px;
      padding: 5px;
    }
    a:hover {
      background: red;
    }
  }
}
.navlogo {
  font-size: 1em;
  cursor: pointer;

  -webkit-user-select: none; /* Safari */
  -webkit-touch-callout: none; /* iOS Safari */
  -khtml-user-select: none; /* Konqueror HTML */
  -ms-user-select: none; /* Internet Explorer/Edge */
  -moz-user-select: none; /* Old versions of Firefox */
  user-select: none;
}
</style>
