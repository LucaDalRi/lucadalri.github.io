<template>
  <span id="langSpan">
    <button :class="isDeutsch ?  'underlined': null" @click="changeLang(true)" class="langBtn">DE</button>
    /
    <button :class="!isDeutsch ?  'underlined': null" @click="changeLang(false)" class="langBtn">IT</button>
  </span>
  <div id="header-container">
    <p style="font-size: 6rem;">Elisa</p>
    <p> &hearts;</p>
    <p style="font-size: 6rem;">Philipp</p>
    <img class="decorazione" src="../assets/image.svg" >
    <p style="font-size: 4rem;">Save the date</p>
    <p style="font-size: 4rem;">20 06 2026</p>
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
  position: relative;
  width: 100vw;
  height: 100dvh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;

  background-image: url("../assets/sfondo-fiori1.svg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  background-attachment: scroll;
  overflow: hidden;
  box-sizing: border-box;
  padding: 2rem;
}

#header-container p {
  margin: 0;
  font-size: 2rem;
  font-family: "MoonTime", cursive;
  color: var(--color-text);
}


#header-container::before {
  content: "";
  position: absolute;
  inset: 0;
  background: rgba(255, 255, 255, 0.5);
  z-index: 1;
}

.decorazione {
  width: 100%;
  max-width: 600px;
  height: auto;
  max-height: 120px;
  display: block;
  margin-bottom: 2.8rem;
  scale: 2.8;
  filter: saturate(0.8);
}



#header-container > * {
  position: relative;
  z-index: 2;
}

#langSpan {
  padding: 10px 10px 0 0;
  display: flex;
  justify-content: end;
  width: 100%;
  font-size: 2rem;
  position: absolute;
  top: 0;
  right: 0;
  z-index: 3;
}

.langBtn {
  color: inherit;
  border: none;
  background-color: transparent;
}

.underlined {
  text-decoration: underline;
}


</style>
