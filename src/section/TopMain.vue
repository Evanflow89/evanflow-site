<template>
  <div>
    <section>
      <div class="bg"></div>
      <h1>Forse</h1>
    </section>
    <section>
      <div class="bg"></div>
      <h1>non ti serve veramente</h1>
    </section>
    <section>
      <div class="bg"></div>
      <h1>un sito web customizzato...</h1>
    </section>
    <section>
      <div class="bg"></div>
      <h1>Ma un sito web customizzato</h1>
    </section>
    <section>
      <div class="bg"></div>
      <h1>è figo, vero?</h1>
    </section>
  </div>
</template>

<script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

export default {
  name: "TopMain",
  mounted() {
    gsap.registerPlugin(ScrollTrigger);

    let getRatio = (el) =>
      window.innerHeight / (window.innerHeight + el.offsetHeight);

    gsap.utils.toArray("section").forEach((section, i) => {
      section.bg = section.querySelector(".bg");

      // Give the backgrounds some random images
      section.bg.style.backgroundImage = `url(https://picsum.photos/1600/800?random=${i})`;

      // the first image (i === 0) should be handled differently because it should start at the very top.
      // use function-based values in order to keep things responsive
      gsap.fromTo(
        section.bg,
        {
          backgroundPosition: () =>
            i ? `50% ${-window.innerHeight * getRatio(section)}px` : "50% 0px",
        },
        {
          backgroundPosition: () =>
            `50% ${window.innerHeight * (1 - getRatio(section))}px`,
          ease: "none",
          scrollTrigger: {
            trigger: section,
            start: () => (i ? "top bottom" : "top top"),
            end: "bottom top",
            scrub: true,
            invalidateOnRefresh: true, // to make it responsive
          },
        }
      );
    });
  },
};
</script>

<style lang="scss">
section {
  position: relative;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}
.bg {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

h1 {
  color: white;
  text-shadow: 1px 1px 3px black;
  z-index: 1;
  font-size: 3em;
  font-weight: 400;
}
</style>