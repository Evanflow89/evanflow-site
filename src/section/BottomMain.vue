<template>
  <section id="Noi">
    <section class="BottomMain d-flex align-items-center">
      <div class="container">
        <div class="row d-flex justify-content-center">
          <div class="col-8 text-center why">
            <h2 class="title text-start">Ottieni Visibilità</h2>
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

    if (window.innerWidth > 576) {
      gsap.to(".title", {
        scrollTrigger: {
          trigger: ".title",
          start: "top center",
          end: "top center",
          once: true,
          scrub: 1,
        },
        x: 100,
        ease: "none",
        duration: 1,
      });
    } else if (window.innerWidth > 1000) {
      gsap.to(".title", {
        scrollTrigger: {
          trigger: ".title",
          start: "top center",
          end: "top center",
          once: true,
          scrub: 1,
        },
        x: 280,
        ease: "none",
        duration: 1,
      });
    } else {
      gsap.to(".title", {
        scrollTrigger: {
          trigger: ".title",
          start: "top center",
          end: "top center",
          once: true,
          scrub: 1,
        },
        x: 40,
        ease: "none",
        duration: 1,
      });
    }
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