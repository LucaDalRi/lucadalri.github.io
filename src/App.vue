<script setup>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Highlights from './components/Highlights.vue'
</script>

<template>
  <div class="wrapper">
    <Header />
    <Main />
    <Highlights />
  </div>
</template>

<script>
export default {
  data() {
    return {}
  },
}
</script>

<style>
.wrapper {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
