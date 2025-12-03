<script setup></script>

<template>
  <content>
    <div id="hero-text">
      <h2>Onde a paisagem vira <span> inspiração. </span></h2>
      <p>
        Explore paisagens, cores e luzes que inspiram novas histórias através da
        fotografia.
      </p>
    </div>
    <img src="../assets/fotografa.jpg" alt="" />
  </content>
</template>

<style scoped>
content {
  font-family: 'Poppins';
  padding: 2rem;
  display: flex;
  img {
    width: 50%;
    border-radius: 3rem;
  }
  #hero-text {
    width: 50%;
    h2 {
      font-size: 3rem;
    }
    span {
      color: #e1306c;
    }
    p {
      margin-top: 1rem;
      font-size: 1.2rem;
    }
  }
}

@media (max-width: 768px) {
  content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    img {
      width: 80%;
      margin-top: 2rem;
      border-radius: 2rem;
    }
    #hero-text {
      width: 100%;
      h2 {
        font-size: 2.5rem;
      }
    }
  }
}
</style>
