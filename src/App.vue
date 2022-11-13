<script setup lang="ts">
import Header from './components/Header.vue'
import PetList from './components/PetList.vue'

export interface Pet {
  id: string
  name: string
  age: number
  image: string
}

const list: Pet[] = [{
  id: '1',
  name: 'Yoshi',
  age: 2,
  image: 'https://picsum.photos/id/1023/600/400',
},
{
  id: '2',
  name: 'Yoshi2',
  age: 3,
  image: 'https://picsum.photos/id/1023/600/400',
},
{
  id: '3',
  name: 'Yoshi3',
  age: 4,
  image: 'https://picsum.photos/id/1023/600/400',
}]
</script>

<template>
  <Header />

  <main>
    <PetList :list="list" />
  </main>
</template>

<style>
main {
  margin-top: 10rem;
  padding: 3rem;
}
</style>