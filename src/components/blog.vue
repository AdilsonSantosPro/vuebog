<template>
    <div class="blog">
        <img :src="imagem.url" alt="Imagem do post" v-if="imagem.url" />
        <h1 :style="{ color: corTitulo }">{{ titulo }}</h1>
        <p>{{ texto }}</p>
    </div>
  </template>
  
  <script>
  // Importe defineProps do Vue.js
  import { defineProps } from 'vue';
  
  export default {
  
  props: {
    titulo: {
      type: String,
      required: false
    },
    texto: {
      type: String,
      required: false
    },
    imagem: {
      type: Object,
      default: () => ({ url: '' }),
      required: false
    },
    
    corTitulo: {
      type: String,
      default: 'orange' 
    }
  }
}
  </script>
  
  <style scoped>

  </style>
  