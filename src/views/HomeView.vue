<script setup>
import { useStore } from '../stores/counter'

const store = useStore()
</script>

<template>
  <div>
    <h1>Welcome home</h1>
    <h1>Count: {{ store.count }}</h1>
    <button @click="store.increment">Increment</button>
  </div>
</template>
