<template>
  <main>
    <h2>Create ToDo</h2>
    <TodoInput @emitTodo="createTodo" />
  </main>
</template>

<script setup>
import { ref } from "vue";
import { uid } from "uid";
import TodoInput from "../components/TodoInput.vue";

const todoList = ref([]);
// const newTodo = ref("");

const createTodo = (todo) => {
  const todoItem = {
    id: uid(),
    todo,
    isCompleted: null,
    isEditing: null,
  };
  console.log(todoItem);
  todoList.value.push(todoItem);
  // newTodo.value = todo;
  // console.log("this is newTodo from the parent", newTodo.value);
};
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
