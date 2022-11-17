<template>
  <section class="BottomMain2">
    <div class="container d-flex align-items-center">
      <div class="row d-flex justify-content-center">
        <div class="col-8 text-center why2">
          <h2 class="title2">
            <span id="create">Affidati ai professionisti</span>
          </h2>
          <p class="pt-4">
            Non ti affideresti ad un tatuatore principiante sapendo che quel
            tatuaggio resterà lì per molto tempo e sarà visibile a tutti. Per il
            tuo sito vale lo stesso concetto!<br />
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
export default {
  name: "BottomMain",
  mounted() {
    gsap.registerPlugin(ScrollTrigger);
    let tl = gsap.timeline({ defaults: { ease: "SlowMo.easeOut" } });
    tl.to("#create", {
      scrollTrigger: {
        trigger: ".title2",
        start: "top center",
        end: "top center",
        once: true,
        scrub: 1,
      },
      y: "0%",
      duration: 0.7,
      stagger: 0.2,
      delay: 0.1,
    });
  },
};
</script>

<style lang="scss" scoped>
.BottomMain2 {
  font-family: "Playfair Display", serif;
  height: 100vh;
  background-image: url("../assets/img/sfondoNoi23.jpg");
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