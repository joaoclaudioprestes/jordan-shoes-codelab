<template>
  <ContainerComponent>
    <div class="boxTitle">
      <h1 class="title">Os melhores em um só lugar</h1>
      <p class="subTitle">A marca Jordan na JordanShoes é a escolha certa para <br> os amantes de sneakers que buscam
        estilo e conforto.</p>
    </div>
    <div class="containerShoes">
      <CardComponent v-for="shoe in shoes" :key="shoe.id" :title="shoe.title" :description="shoe.subTitle"
        :price="shoe.price" :image="shoe.img" :idShoes="shoe.id" />
    </div>
  </ContainerComponent>
</template>

<script>
import CardComponent from '../Card/CardComponent.vue';
import ContainerComponent from '../Container/ContainerComponent.vue';
import shoes from '../../assets/mock/shoes.ts';

export default {
  name: 'ShoesComponent',
  components: {
    ContainerComponent,
    CardComponent
  },
  data() {
    return {
      shoes
    }
  }
}
</script>

<style scoped>
.boxTitle {
  text-align: center;
  margin-top: 2rem;
  margin-top: 80px;
}

.title {
  font-size: 2rem;
  font-weight: 600;
}

.subTitle {
  font-size: 1.5rem;
  font-weight: 400;
  margin-top: 1.5rem;
}

.containerShoes {
  margin-top: 7.4rem;
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 3rem;
  margin-bottom: 8rem;
  grid-auto-rows: auto;
}

@media screen and (max-width: 768px) {
  .containerShoes {
    max-width: 90vw;
    margin: 0 auto;
    margin-bottom: 8rem;
    margin-top: 7.4rem;
  }
}
</style>
