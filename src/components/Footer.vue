<template>
  <div id="footer-container">
    <div>
      <img src="../assets/eliphil2.jpg" id="footer-image" />
      <p>mir freindn ins wennas enk Zeit nemmb</p>
    </div>
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
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
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
#footer-image {
  height: 350px;
  border-radius: 10%;
  margin-top: -150px;
  box-shadow: 0 0 40px 10px rgb(151, 174, 195);
}

p {
  margin: 80px 10px -80px 10px;
  font-size: 3.8rem;
  color: var(--color-text);
  font-family: 'MoonTime', cursive;
}

@media (min-width: 769px) {
  #footer-image {
    height: 500px;
  }
}
</style>
