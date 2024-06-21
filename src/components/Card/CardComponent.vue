<template>
  <div class="card">
    <div class="divImg">
      <img :src="image" alt="" class="img">
    </div>
    <div class="info" :key="idShoes">
      <h1 class="title">{{ title }}</h1>
      <p class="description">{{ description }}</p>
      <p class="price">R$ {{ price }}</p>
    </div>
  </div>
</template>

<script>
import { defineProps } from 'vue'

export default {
  name: 'CardComponent',
  props: {
    title: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    },
    price: {
      type: Number,
      required: true
    },
    image: {
      type: String,
      required: true
    },
    idShoes: {
      type: Number,
      required: true
    }
  }
}
</script>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
}

.divImg {
  width: 384px;
  height: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #F3F7FF;
}

.title {
  font-size: 1.8rem;
  font-weight: 500;
  margin-top: 2.4rem;
}

.description {
  font-size: 1.6rem;
  font-weight: 500;
  margin-top: 1.2rem;
  color: #7CA2F4;
}

.price {
  font-size: 2rem;
  font-weight: 500;
  margin-top: 2.4rem;
}
</style>
