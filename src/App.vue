<template>
  <TodoHeader />
  <RouterView></RouterView>
</template>

<script setup>
import { RouterView } from "vue-router";
import TodoHeader from "./components/TodoHeader.vue";
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
  width: 100%;
  margin: 0 auto;
}
</style>
