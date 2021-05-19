<template>
  <Navigation />
</template>

<script>
import Navigation from "@/components/Navigation.vue";

export default {
  components: {
    Navigation,
  },
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:root {
  background: rgb(0, 3, 34);
  font-size: 1em;
}

//Global Container; use custum in scoped only!
.global_container {
  margin: 0 auto;
  width: 70%;
  padding: 0.5rem;
  color: white;
}
</style>
