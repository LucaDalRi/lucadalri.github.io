<template>
  <div id="main-container">
    <div class="title">
      <img class="heart" src="../assets/heart.png" />
      <h1>Highlights</h1>
    </div>
    <div id="timeline">
      <div class="timeline-line"></div>
      <div class="step" v-for="(item, index) in steps" :key="index">
        <div class="point-wrapper">
          <div class="point"></div>
        </div>
        <a v-if="item.mapIcon" :href="item.a" class="map-link">
          <img v-if="item.icon" :src="item.icon" class="step-icon" />
        </a>
        <img v-if="item.icon && !item.a" :src="item.icon" class="step-icon" />
        <div class="step-content">
          <div class="step-header">
            <span class="step-text">{{ item.time }}</span>
            <a v-if="item.mapIcon" :href="item.a" class="map-link">
              <img :src="item.mapIcon" class="map-icon" />
            </a>
          </div>
          <a v-if="item.a" :href="item.a" class="step-link">
            <span v-if="item.text" class="step-text">{{ item.text }}</span>
          </a>
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
          time: '11:00 Uhr Trauung',
          icon: new URL('../assets/chiesa-icon.png', import.meta.url).href,
          text: 'Kirche Frangart (Eppan)',
          a: 'https://maps.app.goo.gl/prHhXoXT8vaw1Bxj9',
          mapIcon: new URL('../assets/map-icon.png', import.meta.url).href,
        },
        {
          time: '14:00 Uhr Aufbruch',
          icon: new URL('../assets/wedding-car.png', import.meta.url).href,
          text: 'Ansitz Zimmerlehen, Völs am Schlern',
        },
        {
          time: '16:00 Uhr Aperitivo',
          icon: new URL('../assets/aperitivo-icon.png', import.meta.url).href,
          a: 'https://maps.app.goo.gl/chiJpyrFc9eu9YRo9',
          mapIcon: new URL('../assets/map-icon.png', import.meta.url).href,
          text: "Agriturismo Zimmerlehen (Fie' allo Sciliar)",
        },
        {
          time: '18:00 Uhr Essen',
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
  height: 100dvh;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-image: url('../assets/sfondo-fiori1.svg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  overflow-x: hidden;
  background-position: 60%;
  padding-bottom: 20px;
  position: relative;
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
  height: 150px;
  background: linear-gradient(to top, #fff 0%, rgba(255, 255, 255, 0) 100%);
}

#main-container::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 60px;
  background: linear-gradient(to bottom, #fff 0%, rgba(255, 255, 255, 0) 100%);
  z-index: 1;
  pointer-events: none;
}

.title {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 40px;
  padding-top: 20px;
  flex-shrink: 0;
}

.heart {
  height: 50px;
}

#timeline {
  position: relative;
  display: flex;
  flex-direction: column;
  width: 100%;
  padding: 0 20px;
  flex: 1;
  justify-content: space-between;
}

.timeline-line {
  position: absolute;
  left: 29px;
  top: 25px;
  height: calc(100% - 50px);
  width: 3px;
  background-color: #9d7b7b;
  z-index: 1;
  pointer-events: none;
}

.step {
  display: flex;
  align-items: center;
  position: relative;
  z-index: 1;
  min-height: 60px;
}

.point-wrapper {
  margin-right: 15px;
  padding-top: 5px;
}

.point {
  width: 20px;
  height: 20px;
  background-color: #9d7b7b;
  border-radius: 50%;
  box-shadow: 0 0 0 3px rgba(255, 255, 255, 0.8);
}

.step-icon {
  height: 60px;
  width: 60px;
  margin-right: 15px;
  object-fit: contain;
  filter: brightness(0.9) contrast(180%) drop-shadow(0 0 0.2px black);
}

.step-content {
  display: flex;
  flex-direction: column;
  flex: 1;
}

.step-content span {
  font-size: 1.2rem;
  font-weight: 300;
}

.step-header {
  display: flex;
  align-items: center;
  gap: 8px;
  flex-wrap: wrap;
}

.step-text {
  font-size: 1.6rem;
  line-height: 1.3;
}

.map-link {
  display: inline-flex;
  align-items: center;
}

.map-icon {
  width: 40px;
  height: 40px;
  object-fit: contain;
}

.step-link {
  color: inherit;
  text-decoration: none;
}

@media (max-width: 375px) {
  .step-text {
    font-size: 1.4rem;
  }

  .step-icon {
    height: 50px;
    width: 50px;
  }

  .map-icon {
    width: 35px;
    height: 35px;
  }
}

@media (min-width: 769px) {
  #timeline {
    width: 30%;
  }
}

@supports (-webkit-touch-callout: none) {
  #timeline {
    -webkit-box-flex: 1;
  }
}
</style>
