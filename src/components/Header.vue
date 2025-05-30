<template>
  <span id="langSpan">
    <button @click="changeLang(true)" class="langBtn">DE</button>
    /
    <button @click="changeLang(false)" class="langBtn">IT</button>
  </span>
  <div id="header-container">
    <img class="flower-top" src="../assets/illustration_1.jpg" draggable="false" alt="Flower Top">
    <h1>
      <span>ELI</span>
      <span>&middot;</span>
      <span>PHI</span>
    </h1>
    <img class="flower-bottom" src="../assets/illustration_2.jpg" draggable="false" alt="Flower Bottom">
  </div>
</template>

<script>
export default {
  emits: ['changeLang'],
  data() {
    return {
      isDeutsch: true,
    }
  },
  methods: {
    changeLang(deutsch) {
      console.log(deutsch)
      if (deutsch) {
        this.isDeutsch = true
      } else {
        this.isDeutsch = false
      }
      this.$emit('changeLang', this.isDeutsch)
    }
  },
}
</script>

<style scoped>
#header-container {
  display: flex;
  align-items: center;
  flex-direction: column;
  width: 100%;
  height: 100dvh;
  text-align: center;
}

h1 {
  letter-spacing: 0.2rem;
  font-size: 3rem;
}

.flower-top, .flower-bottom .flower-top, .flower-bottom { 
  object-fit: contain;
  width: 90%;
}

.flower-top {
  padding-top: 300px;
}

.flower-bottom {
  padding-bottom: 300px;
}

.langBtn {
  color: inherit;
  border: none;
  background-color: transparent;
}

#langSpan {
  padding: 10px 10px 0 0 ;
  display: flex;
  justify-content: end;
  width: 100%;
}

</style>