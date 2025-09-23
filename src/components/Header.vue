<template>
  <div id="header-container">
    <p style="font-size: 5rem">Elisa</p>
    <img style="height: 50px" src="../assets/heart.png" />
    <p style="font-size: 5rem">Philipp</p>
    <img class="decorazione" src="../assets/image.svg" />
    <p style="font-size: 2.5rem">Save the date!</p>
    <p style="font-size: 2.5rem; display: flex; align-items: center">
      20
      <span style="font-size: 1rem; padding-inline: 0.6rem"> • </span>
      06
      <span style="font-size: 1rem; padding-inline: 0.6rem"> • </span>
      2026
    </p>
    <p style="font-size: 2.5rem; padding: 1rem 0">Weitere Informationen folgen in Kürze</p>
    <p style="font-size: 2.5rem">Bleiben Sie dran!</p>
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
  background-attachment: scroll;
  overflow: hidden;
  box-sizing: border-box;
  padding: 1.4rem;
}

#header-container p {
  margin: 0;
  font-size: 2rem;
  color: var(--color-text);
  text-transform: none;
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
