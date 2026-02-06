<script setup>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Highlights from './components/Highlights.vue'
import Hotels from './components/Hotels.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="wrapper">
    <div class="content">
      <Header />
      <Main />
      <Highlights />
      <Hotels />
      <Footer />
    </div>

    <div id="landscape-warning">Drehen Sie Ihr Telefon vertikal, um fortzufahren 😊</div>
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
  position: relative;
}

.wrapper > .content > * {
  scroll-snap-align: start;
}

#landscape-warning {
  display: none;
  align-items: center;
  justify-content: center;
  position: absolute;
  inset: 0;
  text-align: center;
  background: white;
  color: black;
  font-size: 1.5rem;
  padding: 20px;
  z-index: 1000;
}

@media (max-width: 769px) and (orientation: landscape) {
  .content {
    display: none;
  }

  #landscape-warning {
    display: flex;
  }
}
</style>
