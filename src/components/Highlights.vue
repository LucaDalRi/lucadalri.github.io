<template>
  <div id="main-container">
    <div class="title">
      <img class="heart" src="../assets/heart.png" />
      <h1>Highlights</h1>
    </div>

    <div id="timeline">
      <div class="vertical-line"></div>

      <div class="step" v-for="(item, index) in steps" :key="index">
        <div class="point"></div>
        <img v-if="item.icon" :src="item.icon" class="step-icon" />
        <div class="step-content">
          <span class="step-text">{{ item.time }}</span>
          <span class="step-text" v-if="item.text">{{ item.text }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      steps: [
        {
          time: '11 Uhr Trauung',
          icon: new URL('../assets/chiesa-icon.png', import.meta.url).href,
          text: 'Kirche Frangart (Eppan)',
        },
        {
          time: '14 Uhr Aufbrauch',
          icon: new URL('../assets/wedding-car.png', import.meta.url).href,
          text: 'Ansitz Zimmerlehen, Völs am Schlern',
        },
        {
          time: '16 Uhr Aperitivo',
          icon: new URL('../assets/aperitivo-icon.png', import.meta.url).href,
        },
        {
          time: '18 Uhr Essen',
          icon: new URL('../assets/dish-icon.png', import.meta.url).href,
        },
        {
          time: '21:30 Uhr Party',
          icon: new URL('../assets/dance-icon.png', import.meta.url).href,
        },
        {
          time: 'Gemeinsam ausklingen lassen',
          icon: new URL('../assets/married-icon.png', import.meta.url).href,
        },
      ],
    }
  },
}
</script>

<style scoped>
#main-container {
  background: rgba(255, 255, 255, 0.5);
  width: 100dvw;
  height: 100dvh;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.title {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 40px;
}

.heart {
  height: 50px;
}

#timeline {
  position: relative;
  height: 80%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 0 10px;
}

.vertical-line {
  position: absolute;
  left: 18px;
  top: 20px;
  bottom: 0;
  width: 4px;
  background-color: #9d7b7b;
}

.step {
  display: flex;
  align-items: center;
  position: relative;
  margin-bottom: 85px;
}

.point {
  width: 20px;
  height: 20px;
  background-color: #9d7b7b;
  border-radius: 50%;
  margin-right: 10px;
  z-index: 1;
}

.step:last-child {
  margin-bottom: 0;
}

.step-content {
  display: flex;
  flex-direction: column;
}

.step-icon {
  height: 50px;
  width: 50px;
  margin-right: 10px;
  object-fit: cover;
}

.step-text {
  font-size: 1.6rem;
}
</style>
