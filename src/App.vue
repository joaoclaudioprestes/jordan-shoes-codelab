<script setup lang="ts">
import HeaderComponent from './components/Header/HeaderComponent.vue';
import HeroComponent from './components/Hero/HeroComponent.vue';
import ShoesComponent from './components/Shoes/ShoesComponent.vue';
</script>

<script>

</script>

<template>
  <HeaderComponent />
  <HeroComponent />
  <ShoesComponent />
  <footer>
    <p>
      © 2024 -
      <a href="https://github.com/iuricode/desafios-frontend" class="link" target="_blank">CodeLab</a>
      Challenges - Solved by
    </p>
    <a href="https://jprestes.vercel.app" target="_blank"> <img src="/logo.svg" alt="Logo - João Prestes"
        class="logo" /></a>
  </footer>
</template>

<style scoped>
footer {
  background-color: var(--dark-20);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.4rem;
  color: var(--white);
  font-family: var(--font_inter);
  padding: 1.5rem;
  text-align: center;
  position: static;
  bottom: 0;
  width: 100%;


}

.link {
  color: #ffa500;
  font-weight: 500;
}

.logo {
  width: 3rem;
  height: 3rem;
  margin-left: 4px;
  cursor: pointer;
}
</style>
