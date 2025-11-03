<template>
  <div id="main-container">
    <p>Mir freidn ins wenn es enk am 20.06.2026 Zeit nemmb mit ins, insere Hochzeit zu feiern.</p>
    <img src="../assets/eliphil1.jpeg" class="main-img" />
    <p>
      Olls startet um 11:00 Uhr in do Kirche von
      <a
        style="color: inherit; text-decoration: none"
        href="https://maps.app.goo.gl/prHhXoXT8vaw1Bxj9"
      >
        Frongort (Eppan)
        <img src="../assets/map-icon.png" class="map-icon" />
      </a>
    </p>
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
  background-image: url('../assets/sfondo-fiori1.svg');
  background-size: cover;
  background-position: 27%;
  background-repeat: no-repeat;
  padding: 40px 0;
  position: relative;
}

#main-container::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 60px;
  background: linear-gradient(to bottom, #fff 0%, rgba(255, 255, 255, 0) 100%);
  z-index: 99;
  pointer-events: none;
}

#main-container::before {
  content: '';
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 1;
  pointer-events: none;
  filter: brightness(1.1);
  height: 60px;
  background: linear-gradient(to top, #fff 0%, rgba(255, 255, 255, 0) 100%);
}

#main-container > * {
  position: relative;
  z-index: 3;
}

p {
  padding: 0 10px;
  font-size: 1.8rem;
  font-weight: 300;
  line-height: 2.4rem;
}

.map-icon {
  width: 40px;
  height: 40px;
  object-fit: contain;
  vertical-align: bottom;
}

.main-img {
  box-shadow: 0 0 40px 10px rgb(151, 174, 195);
  border-radius: 10%;
  height: 250px;
}

@media (min-width: 769px) {
  .main-img {
    height: 500px;
  }

  #main-container {
    padding: 120px 0;
  }
}
</style>
