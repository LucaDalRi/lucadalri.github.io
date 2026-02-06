<template>
  <div id="hotels-container">
    <div id="modal" v-if="modalVisible">
      <button @click="closeModal">X</button>
      <p id="modal-text" v-for="text in modalText[selectedModal].text" :key="text">{{ text }}</p>
      <a
        style="text-decoration: none; color: inherit; margin: 10px"
        v-for="link in modalText[selectedModal].links"
        :key="link.name"
        :href="link.url"
      >
        &bull; {{ link.name }}</a
      >
      <p id="modal-text" v-for="info in modalText[selectedModal].info" :key="info">{{ info }}</p>
    </div>
    <div class="icon-container">
      <img v-on:click="openModal('hotel')" src="../assets/hotel-icon.png" class="step-icon" />
      <img v-on:click="openModal('gift')" src="../assets/gift-icon.png" class="step-icon" />
      <img
        v-on:click="openModal('dressCode')"
        src="../assets/dress-code-icon.png"
        class="step-icon"
      />
    </div>
    <h2>Noch Fragen? Klick dich durch</h2>
  </div>
</template>

<script>
export default {
  data() {
    return {
      modalVisible: false,
      selectedModal: null,
      modalText: {
        hotel: {
          text: [
            'Du brauchsch no a Bettl in do Nähe? Koa Problem! ',
            'Wer von enk donoch nimma Hoam fohrn konn odo will konn oanfochn in do Nähe schlofn.',
            'Mir hom für enk schun mol nochgfrog wo a Plotz frei war zun Übonochtn.',
            'De zwoa Orte kanntas unfrogn: ',
          ],
          info: [''],
          links: [
            {
              name: 'Haus Aichner',
              url: 'http://www.hausaichner.it/index.html',
            },
          ],
        },
        gift: {
          text: [
            'Du brauchsch no a Geschenk für do Hochzeitsgäste? Koa Problem! ',
            'Mir hom für enk schun mol no a paar Ideen: ',
          ],
          links: [],
        },
        dressCode: {
          text: [
            'Du brauchst no a Idee für den Dresscode? Koa Problem! ',
            'Mir hom für enk schun mol no a paar Vorschläge: ',
          ],
          links: [],
        },
      },
    }
  },
  methods: {
    openModal(modal) {
      this.selectedModal = modal
      this.modalVisible = true
    },
    closeModal() {
      this.selectedModal = null
      this.modalVisible = false
    },
  },
}
</script>

<style scoped>
#hotels-container {
  background: rgba(255, 255, 255, 0.5);
  position: relative;
  width: 100dvw;
  height: 100dvh;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  background-image: url('../assets/sfondo-fiori1.svg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  padding: 20px 10px;
}

#hotels-container::before {
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

#hotels-container::after {
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

.step-icon {
  height: 70px;
  width: 70px;
  object-fit: cover;
  filter: brightness(0.9) contrast(180%) drop-shadow(0 0 0.2px black);
}

.icon-container {
  display: flex;
  gap: 30px;
  padding-bottom: 40px;
}

#modal {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: white;
  padding: 20px;
  border-radius: 10px;
  z-index: 99;
  min-height: 10%;
  max-height: 60%;
  overflow-y: scroll;
  width: 80%;
  display: flex;
  flex-direction: column;
}

#modal button {
  align-self: flex-end;
  background: transparent;
  border: none;
  font-size: 1rem;
  cursor: pointer;
}

#modal-text {
  margin-top: 20px;
  font-size: 1.2rem;
}

@media (min-width: 769px) {
}
</style>
