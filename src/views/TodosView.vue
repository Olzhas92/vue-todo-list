<template>
  <main>
    <h2>Create ToDo</h2>
    <TodoInput />
  </main>
</template>

<script setup>
import TodoInput from "../components/TodoInput.vue";
</script>

<style lang="scss" scoped>
main {
  display: flex;
  flex-direction: column;
  max-width: 500px;
  width: 100%;
  margin: 0 auto;
  padding: 40px 16px;

  h2 {
    margin-bottom: 16px;
    text-align: center;
  }
}
</style>
