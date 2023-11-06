<template>
  <RouterView></RouterView>
</template>

<script setup>
import { RouterView } from "vue-router";
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@500&family=Roboto:wght@300;400;500;700&display=swap");

* {
  font-family: "Roboto", sans-serif;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.container {
  max-width: 1100px;
  margin: 0 auto;
}
</style>
