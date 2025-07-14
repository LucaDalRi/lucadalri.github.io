<script setup>
import Header from './components/Header.vue'
// import Main from './components/Main.vue'
</script>

<template>
    <div class="wrapper">
      <Header
      @changeLang="($event) => { isDeutsch = $event}"
      />
      <!-- <Main
      :is-Deutsch="isDeutsch"
      /> -->
    </div>
</template>

<script>
export default {
  data() {
    return {
      isDeutsch: true
    }
  },
}
</script>

<style>
.wrapper {
  height: 100vh;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
