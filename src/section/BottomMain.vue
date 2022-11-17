<template>
  <section id="Noi">
    <section class="BottomMain">
      <div class="container d-flex align-items-center">
        <div class="row d-flex justify-content-center">
          <div class="col-8 text-center why">
            <h2 class="title">
              <span id="create2">Ottieni Visibilità</span>
            </h2>
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

import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

export default {
  name: "BottomMain",
  components: {
    BottomMain2,
    ContactUs,
  },
  mounted() {
    gsap.registerPlugin(ScrollTrigger);

    let tl = gsap.timeline({ defaults: { ease: "SlowMo.easeOut" } });
    tl.to("#create2", {
      scrollTrigger: {
        trigger: ".title",
        start: "center center",
        end: "center center",
        scrub: 1,
      },
      y: "0%",
      duration: 0.7,
      stagger: 0.5,
      delay: 5,
    });
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
  font-size: 1.7rem;

  .container {
    background-color: rgba($color: #000000, $alpha: 0.2);
    height: 100%;
    width: 100%;
  }
  h2 {
    font-family: "Playfair Display", serif;
    font-size: 1.7rem;
    background-color: inherit;
    overflow: hidden;
    text-transform: uppercase;
  }

  h2 span {
    display: inline-block;
    transform: translateY(100%);
  }
}
</style>