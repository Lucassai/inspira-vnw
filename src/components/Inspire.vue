<script setup>
import Card from './Card.vue'
</script>

<template>
  <div id="Inspire">
    <h2>Inspire-se</h2>
    <div id="imagens">
      <Card
        imagem="https://images3.alphacoders.com/135/thumbbig-1354394.webp"
      />
      <Card
        imagem="https://images8.alphacoders.com/135/thumbbig-1354384.webp"
      />
      <Card
        imagem="https://images4.alphacoders.com/135/thumbbig-1356514.webp"
      />
      <Card imagem="https://images.alphacoders.com/135/thumbbig-1354383.webp" />
      <Card
        imagem="https://images7.alphacoders.com/134/thumbbig-1343992.webp"
      />
      <Card
        imagem="https://images8.alphacoders.com/134/thumbbig-1348243.webp"
      />
      <Card imagem="https://images.alphacoders.com/135/thumbbig-1358237.webp" />
      <Card imagem="https://images.alphacoders.com/135/thumbbig-1357998.webp" />
      <Card
        imagem="https://images6.alphacoders.com/136/thumbbig-1365621.webp"
      />
      <Card imagem="" />
      <Card imagem="" />
      <Card imagem="" />
      <Card imagem="" />
      <Card imagem="" />
      <Card imagem="" />
    </div>
  </div>
</template>

<style scoped>
#Inspire {
  width: fit-content;
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
</style>
