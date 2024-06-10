<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HomeView from './views/HomeView.vue';
const fetcher = fetch('http://api.nbp.pl/api/exchangerates/tables/a/')
  .then(res => res.json())
  .then(data => this.array = data)
  .catch(err => console.log(err.message))

  preload('/api/user', fetcher)
</script>

<template>
  <RouterView />
</template>

