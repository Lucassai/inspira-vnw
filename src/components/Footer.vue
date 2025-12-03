<script setup>
import {
  IconBrandFacebook,
  IconBrandLinkedin,
  IconBrandTwitter,
  IconBrandInstagram,
} from '@tabler/icons-vue'
</script>

<template>
  <footer>
    <div id="footer-1">
      <div>
        <h4>Contato</h4>
        <li>contato@inspiralens.com</li>
        <li>Central de ajuda</li>
        <li>Rio de Janeiro - Brasil</li>
      </div>
      <div>
        <h4>Sobre</h4>
        <li>Politicas</li>
        <li>Politicas de privacidade</li>
        <li>Blog</li>
      </div>
      <div>
        <h4>Assine nossa newsletter</h4>
        <input id="email" type="email" placeholder="Seu email" />
        <button>Inscreva-se</button>
      </div>
    </div>
    <div id="social-media">
      <li><IconBrandFacebook /></li>
      <li><IconBrandLinkedin /></li>
      <li><IconBrandTwitter /></li>
      <li><IconBrandInstagram /></li>
    </div>
  </footer>
</template>

<style scoped>
footer {
  list-style-type: none;
  padding: 40px 20px;
  font-family: 'Poppins';
  #footer-1 {
    justify-content: space-around;
    display: flex;
  }
  li {
    margin: 10px 0;
  }
  #social-media {
    display: flex;
    justify-content: center;
    margin-top: 20px;
    li {
      margin: 25px 25px;
    }
  }
}
</style>
