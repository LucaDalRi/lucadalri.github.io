<template>
  <div id="main-container">
    <p>Schion dasses di gib!</p>
    <p>Mir freind ins wenn es enk, am 20.06.2026 zeit nemmb mit ins, insre hockzeit zu ferien!</p>
    <p>olles startet un 11 uhr in do kirche von frongort (Eppan)!</p>
    <p>gfeiert werd in völs am schlern!</p>
    <p>Geb ins bitte bis 30. april 2026 bescheid obas dobei seid!</p>
    <div class="bottom-fade"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {}
  },
}
</script>

<style scoped>
#main-container {
  background: rgba(255, 255, 255, 0.5);
  position: relative;
  width: 100dvw;
  height: 100dvh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  overflow: hidden;
}

#main-container::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-image: url('../assets/sfondo-fiori1.svg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  transform: rotate(180deg);
  z-index: 1;
  pointer-events: none;
  filter: brightness(1.2);
}

#main-container::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 50px;
  background: linear-gradient(to bottom, #fff 0%, rgba(255, 255, 255, 0) 100%);
  z-index: 2;
  pointer-events: none;
}

#main-container .bottom-fade {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  height: 50px;
  background: linear-gradient(to top, #fff 0%, rgba(255, 255, 255, 0) 100%);
  z-index: 2;
  pointer-events: none;
}

#main-container > * {
  position: relative;
  z-index: 3;
}

p {
  font-size: 2.4rem;
  line-height: 3rem;
  margin: 0 0 40px;
  padding: 0 20px;
}
</style>
