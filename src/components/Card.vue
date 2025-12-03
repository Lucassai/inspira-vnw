<script setup>
import { IconHeart } from '@tabler/icons-vue'
defineProps(['imagem'])
</script>

<template>
  <div class="card">
    <button>
      <IconHeart color="#e1306c" size="24" />
    </button>
    <img :src="imagem" alt="imagem de teste" />
  </div>
</template>

<style scoped>
.card {
  width: 100%;
  aspect-ratio: 2 / 4;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  border-radius: 1rem;
}

img {
  border-radius: 1rem;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
button {
  background-color: transparent;
  border: none;
  position: absolute;
  top: 10px;
  right: 10px;
  margin: 10px;
  border-radius: 50%;
  padding: 10px;
}
</style>
