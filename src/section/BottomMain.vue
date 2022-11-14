<template>
  <section id="Noi">
    <section class="BottomMain">
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
  </section>
</template>

<script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import BottomMain2 from "../common/BottomMain2.vue";

export default {
  name: "BottomMain",
  components: {
    BottomMain2,
  },
  mounted() {
    gsap.registerPlugin(ScrollTrigger);

    if (window.innerWidth > 576) {
      gsap.to(".why", {
        scrollTrigger: {
          trigger: ".why",
          start: "top 100px",
          end: "top 100px",
          scrub: 1,
        },
        y: 200,
        ease: "none",
        duration: 1,
      });
    } else {
      gsap.to(".why", {
        scrollTrigger: {
          trigger: ".why",
          start: "top 100px",
          end: "top 100px",
          scrub: 1,
        },
        y: 40,
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

  .why2 {
    margin-top: 100px;
  }
}
</style>