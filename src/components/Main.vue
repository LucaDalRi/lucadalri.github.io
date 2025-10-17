<template>
  <div id="main-container">
    <p id="elegant">Schion dasses enk gib!</p>
    <img src="../assets/eliphil1.jpeg" style="height: 150px; border-radius: 10%" />
    <p>Mir freidn ins wenn es enk am 20.06.2026 zeit nemmb mit ins, insere hochzeit zu feiern.</p>
    <img src="../assets/eliphil2.jpg" style="height: 150px; border-radius: 10%" />
    <p>Olls startet um 11:00 Uhr in do kirche von Frongort (Eppan).</p>
    <!-- <p>Gfeiert werd in völs am schlern!</p>
    <p>Geb ins bitte bis 30. April 2026 bescheid obas dobei seid!</p> -->
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
  justify-content: space-evenly;
  text-align: center;
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
  height: 80px;
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

#elegant {
  font-family: 'MoonTime', cursive;
  font-size: 3.6rem;
  margin: 0;
  padding: 0 20px;
}

p {
  padding: 0 10px;
  font-size: 2rem;
  font-weight: 300;
  line-height: 2.4rem;
}

img {
  margin: 10px 0;
}
</style>
