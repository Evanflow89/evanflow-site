<template>
  <section class="BottomMain">
    <div class="container">
      <div class="row">
        <div class="col-12 text-center">
          <h2 class="why">Testo</h2>
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

    gsap.to(".why", {
      scrollTrigger: {
        trigger: ".why",
        start: "top center",
        end: "top 200px",
        scrub: 1,
      },
      y: 400,
      ease: "none",
      duration: 2,
    });
  },
};
</script>

<style lang="scss" scoped>
.BottomMain {
  height: 100vh;
  background-color: black;
  color: white;
}
</style>