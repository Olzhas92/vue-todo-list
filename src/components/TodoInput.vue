<template>
  <div class="form">
    <input type="text" placeholder="Add ToDo" v-model="todo" />
    <button @click="createTodo">Create</button>
  </div>
</template>

<script setup>
import { ref, defineEmits } from "vue";
const todo = ref("");

const emit = defineEmits(["emitTodo"]);

const createTodo = () => {
  if (!todo.value) {
    console.log("no todo");
    return;
  } else {
    emit("emitTodo", todo.value);
  }
};
</script>

<style lang="scss" scoped>
.form {
  display: flex;
  transition: 250ms ease;
  border: 2px solid #41b080;

  &:focus-within {
    box-shadow: 0 -4px 6px -1px rgb(0 0 0 / 0.1),
      0 -2px 4px -2px rgb(0 0 0 / 0.1);
  }

  input {
    width: 100%;
    padding: 8px 6px;
    border: none;

    &:focus {
      outline: none;
    }
  }

  button {
    padding: 8px 16px;
    border: none;
    cursor: pointer;

    &:hover {
      background-color: lightcoral;
      color: #fff;
    }
  }
}
</style>
