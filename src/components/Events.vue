<template>
  <div class="row">
    <div class="col-1 mx-auto text-center">
      <img
        class="img-fluid"
        src="../assets/img/upcoming-events-calendar-icon.png"
        alt="clock-and-bell"
      />
    </div>
    <h2 class="mt-3 col-12 text-center font-35 text-white">
      <span>Upcoming Events</span>
    </h2>
    <div class="col-12">
      <div class="row justify-content-center my-5">
        <EventsCard
          v-for="(card, index) in cards"
          :key="index"
          :title="card.title"
          :date="card.date"
          :text="card.text"
          :buttonText="card.buttonText"
          :buttonColor="card.buttonColor"
        />
      </div>
      <div class="col-12 text-center my-5 py-5">
        <a class="big-button text-white bg-yellow" href="#">View all events</a>
      </div>
    </div>
  </div>
</template>

<script>
import EventsCard from "./EventsCard.vue";
export default {
  name: "events",
  components: {
    EventsCard,
  },
  data() {
    return {
      cards: [
        //^DATO CHE LA SOLA COSA CHE CAMBIA E' LA DATA AVREI POTUTO FAR VEDERE TUTTI GLI ALTRI ELEMENTI IN MODO STATICO E METTERE SOLO L'OGGETTO DATA, MA HO
        //^VOLUTO SIMULARE L'EVENTUALITA' CHE LE CARD FOSSERO TUTTE DIVERSE, COSI ANCHE NEL CASO CHE DOVESSERO CAMBIARE UN GIORNO BASTERA INSERIRE I DATI DEGLI OGGETTI SENZA DOVER CREARE UN NUOVO TEMPLATE.
        {
          title: "Coaching Session",
          date: "20 May 21:30 PM",
          text: "Lorem ipsum dolor sit amet, consecteur adipiscing elit, sed do eiusmod tempor [...]",
          buttonText: "Find More",
          buttonColor: "bg-color-primary",
        },
        {
          title: "Coaching Session",
          date: "20 May 21:30 PM",
          text: "Lorem ipsum dolor sit amet, consecteur adipiscing elit, sed do eiusmod tempor [...]",
          buttonText: "Find More",
          buttonColor: "bg-color-primary",
        },
        {
          title: "Coaching Session",
          date: "20 May 21:30 PM",
          text: "Lorem ipsum dolor sit amet, consecteur adipiscing elit, sed do eiusmod tempor [...]",
          buttonText: "Find More",
          buttonColor: "bg-color-primary",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
</style>