<script setup>
import { ref } from 'vue'
import { IconSearch, IconUser, IconMenu3 } from '@tabler/icons-vue'

const menuOpen = ref(false)

const toggleMenu = () => {
  menuOpen.value = !menuOpen.value
}
</script>

<template>
  <div id="Header">
    <img src="../assets/icon.svg" alt="" />

    <div id="menu">
      <ul>
        <li>
          <a href=""><IconSearch size="36px" /></a>
        </li>
        <li><a href="">Início</a></li>
        <li><a href="">Galeria</a></li>
        <li><a href="">Favoritos</a></li>
        <li>
          <a href=""><IconUser color="red" size="36px" /></a>
        </li>
      </ul>
    </div>
    <div id="menu-hamburguer">
      <a href=""><IconSearch size="36px" /></a>
      <button id="menu-hamburguer-btn" @click="toggleMenu">
        <IconMenu3 />
      </button>
      <div id="menu-dropdown" v-show="menuOpen">
        <ul>
          <li><a href="">Início</a></li>
          <li><a href="">Galeria</a></li>
          <li><a href="">Favoritos</a></li>
          <li>
            <a href=""><IconUser color="red" size="36px" /></a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style scoped>
#Header {
  font-family: 'Poppins';
  display: flex;
  padding: 10px 20px;
  justify-content: space-between;
  margin: 20px;

  ul {
    align-items: center;
    display: flex;
    li {
      text-align: center;
      padding: 0 30px;
      list-style-type: none;
      a {
        text-decoration: none;
        color: black;
      }
    }
  }
}

#menu-hamburguer {
  display: none;
  position: relative;
}

#menu-hamburguer a {
  color: black;
}

#menu-hamburguer-btn {
  display: none;
  background: none;
  border: none;
  cursor: pointer;
  padding: 0;
}
#menu-dropdown {
  display: block;
  position: absolute;
  left: -50px;
  top: 45px;
  background-color: white;
  box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
  z-index: 1;
  ul {
    flex-direction: column;
    li {
      padding: 12px 16px;
      text-align: left;
    }
  }
}
#menu-dropdown[style*='display: none'] {
  display: none !important;
}
#menu-dropdown:not([style*='display: none']) {
  display: block !important;
}
@media (max-width: 768px) {
  #menu {
    display: none;
  }
  #menu-hamburguer {
    display: flex;
    align-items: center;
    gap: 15px;
  }
  #menu-hamburguer-btn {
    display: block;
    color: black;
  }
}
</style>
