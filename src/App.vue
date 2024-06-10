<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HomeView from './views/HomeView.vue'
import useSWR from 'swr'

const fetcher = fetch('http://api.nbp.pl/api/exchangerates/tables/a/')
  .then(res => res.json())
  .then(data => this.array = data)
  .catch(err => console.log(err.message))
function Profile() {
  const { data, error, isLoading } = useSWR('http://api.nbp.pl/api/exchangerates/tables/a/', fetcher)
 
  if (error) return <div>failed to load</div>
  if (isLoading) return <div>loading...</div>
  return <div>hello {data.name}!</div>
}

Profile()
</script>

<template>
  <RouterView />
</template>

