<script setup lang="ts">
import type { Pet } from '@/App.vue';

const props = defineProps<{
    pet: Pet
}>()

</script>

<template>
    <div class="pet-card">
        <img :src="props.pet.image" alt="Image">
        <h3>{{ props.pet.name }}</h3>
        <p>Age: {{ props.pet.age }} years old</p>
        <div class="buttons">
            <button class="edit">
                <i class="ph-pencil" />
                <span>Edit</span>
            </button>
            <button class="delete">
                <i class="ph-x" />
                <span>Delete</span>
            </button>
        </div>
    </div>
</template>

<style>
.pet-card {
    width: 25rem;
    padding: 2rem;
    display: flex;
    align-items: center;
    cursor: pointer;
    border-radius: 8px;
    box-shadow: 0 0 4px 2px rgba(0, 0, 0, .1);
    flex-direction: column;
    transition: .15s ease;
    border: 2px solid rgb(68, 68, 68);
    background-color: #dedede;
}

.pet-card:hover {
    transform: scale(1.05);
}

.pet-card img {
    margin-bottom: 1.5rem;
    border-radius: 8px;
    width: 100%;
}

.pet-card h3,
.pet-card p,
.pet-card .buttons button {
    font-family: "Nunito", sans-serif;
}

.pet-card h3 {
    font-size: 2rem;
    font-weight: 700;
    color: #191919;
    margin-bottom: 1rem;
}

.pet-card p {
    font-weight: 500;
    font-size: 1.8rem;
    margin-bottom: 1.5rem;
    color: #303030;
}

.pet-card .buttons {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    width: 100%;
}

.pet-card .buttons button {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 1.5rem;
    padding: 1rem;
    width: 100%;
    border-radius: 6px;
    font-size: 1.7rem;
    cursor: pointer;
    font-weight: 500;
    border: 0;
    color: #fff;
    transition: .15s ease;
}

.pet-card .buttons button{
    font-size: 2rem;
    color: #fff;
}

.pet-card .buttons button:hover {
    filter: brightness(.8);
}

.pet-card .buttons .edit {
    background: #22c;
}

.pet-card .buttons .delete {
    background: #ff4949;
}
</style>