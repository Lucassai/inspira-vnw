<script setup>
import Card from './Card.vue'

const cards = Array.from({ length: 20 }, (_, i) => ({
  id: 300 + i,
  imagem: `https://picsum.photos/id/${500 + i}/1920/1080`,
}))
</script>

<template>
  <div id="Inspire">
    <h2>Inspire-se</h2>
    <div id="imagens">
      <Card v-for="card in cards" :key="card.id" :imagem="card.imagem" />
    </div>
  </div>
</template>

<style scoped>
#Inspire {
  width: 100%;
  font-family: 'Poppins';
  margin: 40px 20px;
  h2 {
    margin-bottom: 20px;
  }
}
#imagens {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
}

@media (max-width: 1200px) {
  #imagens {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (max-width: 768px) {
  #imagens {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 480px) {
  #imagens {
    grid-template-columns: 1fr;
  }
}
</style>
