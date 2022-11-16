<template>
  <section id="Noi">
    <section class="BottomMain d-flex align-items-center">
      <div class="container">
        <div class="row d-flex justify-content-center">
          <div class="col-8 text-center why">
            <h2>Ottieni Visibilità</h2>
            <p class="pt-4">
              Qualsiasi sia la tua attività, che si tratti di un bar, un
              ristorante o un'azienda, è importante avere una presenza ben
              marcata sul web. Per questo un sito personale ti viene in aiuto!
            </p>
          </div>
        </div>
      </div>
    </section>
    <BottomMain2 />
    <ContactUs />
  </section>
</template>

<script>
import BottomMain2 from "../common/BottomMain2.vue";
import ContactUs from "../common/ContactUs.vue";

export default {
  name: "BottomMain",
  components: {
    BottomMain2,
    ContactUs,
  },
};
</script>

<style lang="scss" scoped>
.BottomMain {
  font-family: "Playfair Display", serif;
  height: 100vh;
  background-image: url("../assets/img/sfondoNoi.jpg");
  background-size: cover;
  color: white;
  font-size: 2rem;
  h2 {
    font-family: "Playfair Display", serif;
    font-size: 2.4rem;
  }
}
</style>