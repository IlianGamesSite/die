<template>
  <div class="app">
  <header>
    <Header />
  </header>
    <Main />
    <place />
    <number />
    <graphick />
  </div>
</template>

<script>
import Header from './components/header.vue'
import Main from './components/main.vue'
import place from './components/place.vue'
import number from './components/number.vue'
import graphick from './components/graphick.vue'

export default {
  components: {
    Header,
    Main ,
    place ,
    number ,
    graphick
  }
}
</script>

<style scoped>
.app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: stretch;

  background: url('/images/background.jpeg') center top / 100% auto no-repeat;
  background-attachment: fixed;
  background-color: #000; /* фон вокруг, если по высоте не хватает */
  color: #fff;
  padding: 60px 20px;
  text-align: center;
  font-family: Arial, sans-serif;
  overflow: hidden;
}

body {
  font-size: 18px; /* Увеличь размер текста по умолчанию */
}

/* Анимация движения градиента */
@keyframes bgShift {
  0% {
    /* background-position: 0% 50%; */
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}

/* Адаптивность для мобильных устройств */
@media (max-width: 600px) {
  .app {
    padding: 0 8px;
  }

  header {
    flex-direction: column;
    align-items: flex-start;
    padding: 10px 0;
  }

}
</style>
