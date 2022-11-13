<script setup lang="ts"></script>

<template>
  <header>
    <a class="logo" href="/">Pets Manager</a>

    <button class="new-pet">
      <i class="ph-plus" color="#fff"></i>
    </button>
  </header>
</template>

<style>
header {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 100;
  width: 100%;
  display: flex;
  box-shadow: 0px 0px 4px 2px rgba(0,0,0,0.5);
  align-items: center;
  justify-content: space-between;
  padding: 25px;
  background: #5941a9;
}

header .logo {
  color: #fff;
  font-family: "Nunito", sans-serif;
  font-size: 1.8rem;
  letter-spacing: .3rem;
  text-transform: uppercase;
  text-decoration: none;
  position: relative;
  font-weight: 700;
}

header .logo::after {
  content: "";
  transform: scaleX(0);
  transition: .175s ease-out;
  background: #fff;
  height: 3px;
  width: 100%;
  position: absolute;
  left: 0;
  bottom: -.5rem;
}

header .logo:hover::after {
  transform: scaleX(.8);
}

header .new-pet {
  border: 0;
  padding: .5rem;
  background-color: rgba(255,255,255,0);
  cursor: pointer;
  transition: .15s ease;
}

header .new-pet i {
  font-size: 2.8rem;
  color: #fff;
}

header .new-pet:hover {
  background-color: rgba(255,255,255,0.15);
}
</style>
