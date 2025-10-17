<template>
  <div id="footer-container">
    <img src="../assets/eliphil1.jpg" class="footer-img top" />
    <p class="footer-text">Mir freidn ins!</p>
    <img src="../assets/heart.png" class="small-heart" />
    <p class="footer-text names">Elisa & Philipp</p>
    <img src="../assets/eliphil2.jpg" class="footer-img bottom" />
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
#footer-container {
  position: relative;
  width: 100dvw;
  height: 100dvh;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
}

#footer-container::before {
  content: '';
  position: absolute;
  inset: 0;
  background-image: url('../assets/sfondo-fiori1.svg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  transform: rotate(180deg);
  z-index: 1;
  pointer-events: none;
  filter: brightness(1.2);
}

#footer-container::after {
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

.footer-img {
  width: 50%;
  height: 50%;
  z-index: 1;
}

.footer-img.top {
  margin-bottom: 10px;
}

.footer-img.bottom {
  margin-top: 10px;
}

.footer-text {
  font-size: 2.4rem;
  margin: 5px 0;
  z-index: 3;
}

.footer-text.names {
  margin: 10px 0;
}

.small-heart {
  height: 50px;
  margin: 5px 0;
  z-index: 3;
}
</style>
