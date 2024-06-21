<template>
  <ContainerComponent>
    <div class="boxTitle">
      <h1 class="title">{{ title }}</h1>
      <p class="subTitle">{{ description }}</p>
    </div>
    <div class="containerShoes">
      <div v-for="shoe in shoes" :key="shoe.id">
        <CardComponent :title="shoe.title" :description="shoe.subTitle" :price="shoe.price" :image="shoe.img"
          :idShoes="shoe.id" />
      </div>
    </div>
  </ContainerComponent>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import CardComponent from '../Card/CardComponent.vue';
import ContainerComponent from '../Container/ContainerComponent.vue';
import shoes from '../../assets/mock/shoes';

export default defineComponent({
  name: 'ShoesComponent',
  components: {
    CardComponent,
    ContainerComponent
  },
  data() {
    return {
      shoes: shoes
    };
  },
  props: {
    title: String,
    description: String
  }
});
</script>

<style scoped>
.boxTitle {
  text-align: center;
  margin-top: 2rem;
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
