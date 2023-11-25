<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { useStore } from './stores/counter'

const store = useStore()
</script>

<template>
  <div>
    <header>My header</header>
    <nav>
      <div class="top-nav" v-if="!store.isLoggedIn">
        <RouterLink to="/"  class="nav-item">Home</RouterLink>
        <RouterLink to="/about" class="nav-item">About</RouterLink>
        <RouterLink to="/login" class="nav-item">Login</RouterLink>
        <RouterLink to="/signup" class="nav-item">Signup</RouterLink>
      </div>
    </nav>

    <router-view/>
  </div>
</template>

<style scoped>
.nav-item{
  padding: 14px 28px;
}

</style>