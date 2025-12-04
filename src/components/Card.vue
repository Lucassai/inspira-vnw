<script setup>
import { IconHeart, IconHeartFilled } from '@tabler/icons-vue'

defineProps(['imagem', 'alt'])

const heartClicked = () => {
  const heartIcon = event.currentTarget.querySelector('#heartIcon')
  const heartFilledIcon = event.currentTarget.querySelector('#heartFilledIcon')

  if (heartIcon.style.display !== 'none') {
    heartIcon.style.display = 'none'
    heartFilledIcon.style.display = 'block'
  } else {
    heartIcon.style.display = 'block'
    heartFilledIcon.style.display = 'none'
  }
}
</script>

<template>
  <div @click="heartClicked" class="card">
    <button>
      <IconHeart id="heartIcon" color="#e1306c" display="block" />
      <IconHeartFilled id="heartFilledIcon" color="#e1306c" display="none" />
    </button>
    <img :src="imagem" :alt="alt" />
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
.card:hover {
  cursor: pointer;
  transform: scale(1.05);
  transition: transform 0.3s ease;
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
