<template>
  <div id="header-container">
    <p style="font-size: 7rem">Elisa</p>
    <img style="height: 70px" src="../assets/heart.png" />
    <p style="font-size: 7rem">Philipp</p>
    <img class="decorazione" src="../assets/image.svg" />
    <span style="font-size: 2rem; font-weight: 300; display: flex; align-items: center">
      20
      <span style="font-size: 1rem; padding-inline: 0.6rem"> • </span>
      06
      <span style="font-size: 1rem; padding-inline: 0.6rem"> • </span>
      2026
    </span>
  </div>
</template>

<script>
export default {
  data() {
    return {}
  },
  methods: {},
}
</script>

<style scoped>
#header-container {
  position: relative;
  width: 100dvw;
  height: 100dvh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;

  background-image: url('../assets/sfondo-fiori1.svg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  overflow: hidden;
  padding: 1.4rem;
  box-sizing: border-box;
}

#header-container::after {
  content: '';
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  height: 50px;
  background: linear-gradient(to bottom, rgba(255, 255, 255, 0) 0%, #fff 100%);
  pointer-events: none;
}

#header-container > * {
  position: relative;
  z-index: 3;
}

#header-container p {
  margin: 0;
  font-size: 2rem;
  color: var(--color-text);
  text-transform: none;
  font-family: 'MoonTime', cursive;
}

#header-container span {
  padding: 8px 0;
}

#header-container::before {
  content: '';
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
</style>
