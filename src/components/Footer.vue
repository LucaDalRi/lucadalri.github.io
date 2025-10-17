<template>
  <div id="footer-container">
    <!-- TESTO CURVATO -->
    <svg width="400" height="150" viewBox="0 0 400 150">
      <defs>
        <!-- controlla qui la curvatura modificando "A" (raggio e angolo) -->
        <path id="semicurve" d="M 50,120 A 150,80 0 0,1 350,120" fill="none" />
      </defs>

      <text font-size="60" font-family="MoonTime, cursive" fill="var(--color-text)">
        <textPath href="#semicurve" startOffset="50%" text-anchor="middle">
          Schion dasses enk gib!
        </textPath>
      </text>
    </svg>

    <!-- IMMAGINE -->
    <img
      src="../assets/eliphil2.jpg"
      style="height: 300px; border-radius: 10%; margin-top: -150px"
    />
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
#footer-container {
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
  background-position: center;
  background-repeat: no-repeat;
}

#footer-container::before {
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

#footer-container::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 60px;
  background: linear-gradient(to top, #fff 0%, rgba(255, 255, 255, 0) 100%);
  z-index: 99;
  pointer-events: none;
}
</style>
