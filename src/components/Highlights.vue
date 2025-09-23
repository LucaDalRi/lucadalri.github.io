<template>
  <div id="main-container">
    <img style="height: 50px" src="../assets/heart.png" />
    <h1>Highlights</h1>
    <div style="width: 100px; padding-top: 50px">
      <div class="point" style="top: 10px">
        <div style="left: 30px; position: absolute; width: 160px; border: 2px solid red">
          <span>11 uhr trauung</span>
          <img style="height: 50px" src="../assets/chiesa-icon.png" />
          <p>
            <span>Kirche Frangart (Eppan)</span>
            <img style="height: 50px" src="../assets/hands-icon.png" />
          </p>
        </div>
      </div>
      <div class="point" style="top: 110px">
        <div style="right: 60px; width: 140px; position: absolute; border: 2px solid red">
          <span>14 Uhr aufbrauch</span>
          <img style="height: 50px" src="../assets/wedding-car.png" />
          <span>Ansitz zimmerlehen, Vols am schlern</span>
        </div>
      </div>
      <div class="point" style="top: 210px">
        <div style="left: 65px; width: 140px; position: absolute; border: 2px solid red">
          <span>16 uhr aperitivo</span>
          <img style="height: 50px" src="../assets/aperitivo-icon.png" />
        </div>
      </div>
      <div class="point" style="top: 310px">
        <div style="right: 60px; width: 140px; position: absolute; border: 2px solid red">
          <span>18 uhr essen</span>
          <img style="height: 50px" src="../assets/dish-icon.png" />
        </div>
      </div>
      <div class="point" style="top: 410px">
        <div style="left: 75px; width: 140px; position: absolute; border: 2px solid red">
          <span>21:30 uhr party</span>
          <img style="height: 50px" src="../assets/dance-icon.png" />
        </div>
      </div>
      <div class="point" style="top: 510px">
        <div style="right: 60px; width: 160px; position: absolute; border: 2px solid red">
          <span>Gemeinsam ausklingen lessen</span>
          <img style="height: 50px" src="../assets/married-icon.png" />
        </div>
      </div>
      <div id="vertical-line"></div>
      <div class="horizontal-line" style="top: -582px"></div>
      <div class="horizontal-line" style="left: 48px; top: -466px"></div>
      <div class="horizontal-line" style="top: -350px"></div>
      <div class="horizontal-line" style="left: 48px; top: -234px"></div>
    </div>
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
  width: 100dvw;
  height: 100dvh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.point {
  width: 20px;
  height: 20px;
  background-color: black;
  border-radius: 50%;
  position: relative;
  left: 40px;
}

#vertical-line {
  position: relative;
  top: -100px;
  width: 4px;
  height: 600px;
  background-color: black;
  margin: 0 auto;
}

.horizontal-line {
  position: relative;
  width: 60px;
  height: 4px;
  background-color: black;
  position: relative;
  border-radius: 50px;
}
</style>
