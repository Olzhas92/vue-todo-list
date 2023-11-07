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
  background-color: lightcoral;

  .container {
    display: flex;
    align-items: center;
    padding: 25px 16px;

    &__branding {
      display: flex;
      align-items: center;
      gap: 16px;
      text-decoration: none;
      color: #000000;

      img {
        max-width: 48px;
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
      flex: 1;
      align-items: center;
      justify-content: flex-end;
      gap: 16px;

      list-style: none;
      text-decoration: none;
      &--home,
      &--about {
        min-height: 20px;
        a {
          text-decoration: none;
          color: #000000;
          font-weight: 500;

          &:hover {
            color: #ffffff;
          }
        }

        &:hover {
          cursor: pointer;
          border-bottom: 1px solid blue;
        }
      }
    }
  }
}
</style>
