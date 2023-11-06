<template>
  <header>
    <nav class="container">
      <RouterLink to="/" class="container__branding">
        <img src="../assets/to-do-list.png" />
        <h1>ToDo List</h1>
      </RouterLink>
      <ul class="container__nav-routes">
        <li class="container__nav-routes--home">
          <RouterLink to="/">Home</RouterLink>
        </li>
        <li class="container__nav-routes--about">
          <RouterLink to="/about">About</RouterLink>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script setup>
import { RouterLink } from "vue-router";
</script>

<style lang="scss" scoped>
header {
  background-color: lightgray;

  .container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    padding: 16px 110px;

    .container__branding {
      display: flex;
      align-items: center;
      justify-content: flex-start;
      gap: 16px;
      width: 30%;
      text-decoration: none;
      color: #000000;
      img {
        width: 24px;
        height: auto;
        cursor: pointer;
      }

      h1 {
        font-size: 24px;
        cursor: pointer;
      }
    }

    &__nav-routes {
      display: flex;
      align-items: center;
      justify-content: space-between;
      width: 20%;
      list-style: none;
      text-decoration: none;
      &--home,
      &--about {
        min-height: 20px;
        a {
          text-decoration: none;
          color: #000000;
        }

        &:hover {
          cursor: pointer;
          border-bottom: 1px solid red;
        }
      }
    }
  }
}
</style>
