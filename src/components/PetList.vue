<script setup lang="ts">
import PetCard from './PetCard.vue'
import type { Pet } from '@/App.vue';
import { defineProps } from 'vue';

const props = defineProps<{
    list: Pet[]
}>()
</script>

<template>
    <section class="pet-list">
        <PetCard v-for="pet in props.list" :key="pet.id" :pet="pet" />
    </section>
</template>

<style>
.pet-list {
    display: flex;
    width: 100%;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
}
</style>