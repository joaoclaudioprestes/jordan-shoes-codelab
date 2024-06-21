<script setup lang="ts">

</script>

<template>
  <div class="divBg">
    <div class="container">
      <div class="box">
        <img src="../../assets/img/logo.svg" alt="Logo Nike" />
        <div>
          <p class="title">A melhor loja de Jordan</p>
          <p class="subTitle">O tênis Jordan é fruto de uma velha e forte <br> parceria entre a Nike e o jogador Michael
            Jordan.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.divBg {
  width: 100%;
  height: 400px;
  background-image: url("../../assets/img/image-michael-jordan.png");
  background-size: cover;
}

.container {
  max-width: 1216px;
  height: 100%;
  margin: 0 auto;
  display: flex;
  justify-content: start;
  align-items: center;
  color: #fff;
}

.title {
  font-size: 2rem;
  font-weight: 500;
  margin-top: 2.5rem;
}

.subTitle {
  font-size: 1.5rem;
  font-weight: 400;
  margin-top: 1.25rem;
}

@media screen and (max-width: 768px) {
  .container {
    max-width: 90vw;
  }
}
</style>


<script>
export default {
  name: 'HeroComponent'
}
</script>