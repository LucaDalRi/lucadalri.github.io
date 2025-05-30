<template>
    <div v-if="!isDeutsch" id="main-container">
      <p>Quest'anno festeggeremo il nostro matrimonio!</p>
      <h1>12 &middot; 12 &middot; 26</h1>
      <img draggable="false" src="../assets/illustration_3.jpg" alt="Illustrazione matrimonio">
      
      <p>Cerimonia - Ore 15:00</p>
      <p>
        Maso Gesù Cristo<br>
        V. Marco Togno, 1 &middot; 39100<br>
        Bolzano (BZ)
      </p>
      
      <img draggable="false" src="../assets/illustration_5.jpg" alt="Illustrazione aperitivo">
      
      <p>Aperitivo &middot; Cena &middot; Party - Dalle ore 17:30</p>
      <p>
        Agriturismo della Madonna<br>
        V. Colle Storto, 111 &middot; 39100<br>
        Bolzano (BZ)
      </p>
      
      <img draggable="false" src="../assets/illustration_6.jpg" alt="Illustrazione conferma">
      
      <p>
        Per confermare la tua presenza e quella dei tuoi accompagnatori, 
        scrivici su WhatsApp entro il 20 maggio.<br>
        Puoi anche comunicarci eventuali esigenze alimentari.
      </p>
      
      <img draggable="false" src="../assets/illustration_4.jpg" alt="Illustrazione regalo">
      
      <p>
        Il regalo più bello sarà la tua presenza nel nostro giorno speciale. 
        Se desideri farci un dono, preferiamo un contributo per il nostro futuro. 
        Quando lo useremo, penseremo a te con affetto.
      </p>
      
      <img draggable="false" src="../assets/illustration_5.jpg" alt="Illustrazione emozione">
      
      <p>Non vediamo l’ora di condividere questo giorno con te!</p>
    </div>
    
    <div v-else id="main-container">
      <p>Dieses Jahr werden wir unsere Hochzeit feiern!</p>
      <h1>12 &middot; 12 &middot; 26</h1>
      <img draggable="false" src="../assets/illustration_3.jpg" alt="Hochzeitsillustration">

      <p>Zeremonie - Um 15:00 Uhr</p>
      <p>
        Maso Gesù Cristo<br>
        V. Marco Togno, 1 &middot; 39100<br>
        Bozen (BZ)
      </p>

      <img draggable="false" src="../assets/illustration_5.jpg" alt="Aperitif-Illustration">

      <p>Aperitif &middot; Abendessen &middot; Party - Ab 17:30 Uhr</p>
      <p>
        Agriturismo della Madonna<br>
        V. Colle Storto, 111 &middot; 39100<br>
        Bozen (BZ)
      </p>

      <img draggable="false" src="../assets/illustration_6.jpg" alt="Bestätigungsillustration">

      <p>
        Um deine Anwesenheit und die deiner Begleitpersonen zu bestätigen, 
        schreib uns bitte bis zum 20. Mai auf WhatsApp.<br>
        Du kannst uns auch eventuelle Ernährungsbedürfnisse mitteilen.
      </p>

      <img draggable="false" src="../assets/illustration_4.jpg" alt="Geschenkillustration">

      <p>
        Das schönste Geschenk ist deine Anwesenheit an unserem besonderen Tag. 
        Wenn du uns trotzdem etwas schenken möchtest, freuen wir uns über einen Beitrag für unsere Zukunft. 
        Wenn wir ihn nutzen, werden wir liebevoll an dich denken.
      </p>

      <img draggable="false" src="../assets/illustration_5.jpg" alt="Emotionale Illustration">

      <p>Wir können es kaum erwarten, diesen Tag mit dir zu teilen!</p>
  </div>

  </template>
  
  <script>
  export default {
    props: {
      isDeutsch: Boolean
    },
    data() {
      return {
      }
    },
  }
  </script>

  <style scoped>
#main-container {
  min-height: 100dvh;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  flex-direction: column;
  text-align: center;
  padding: 0 10px; /* poca spaziatura laterale */
}

p {
  font-size: 2.2rem;
  line-height: 3.2rem;
  margin: 0 0 60px;
  padding: 0 10px; /* padding laterale ridotto */
}

h1 {
  padding-bottom: 60px;
  margin-top: 20px;
}

img {
  object-fit: contain;
  width: 90%;
  padding-bottom: 60px;
}

  </style>
  