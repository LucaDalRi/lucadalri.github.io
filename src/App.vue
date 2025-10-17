<script setup>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Highlights from './components/Highlights.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="wrapper">
    <Header />
    <Main />
    <Highlights />
    <Footer />
  </div>
</template>

<style>
.wrapper {
  margin: 0;
  padding: 0;
  box-sizing: border-box;

  height: 100dvh;
  overflow-y: scroll;
  scroll-snap-type: y mandatory;
  -webkit-overflow-scrolling: touch;
}

.wrapper > * {
  scroll-snap-align: start;
}
</style>
