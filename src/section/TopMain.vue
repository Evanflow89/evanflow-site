<template>
  <div id="Home">
    <section>
      <div class="bg one"></div>
      <h1 class="text-center">
        <span class="hi">Ciao, sono</span>
        <span class="text"></span>
        <span class="cursor">_</span>
      </h1>
    </section>
  </div>
</template>

<script>
import { gsap } from "gsap";
import { TextPlugin } from "gsap/TextPlugin";

export default {
  name: "TopMain",
  mounted() {
    const words = [
      "Ivan.",
      "Un Milionario.",
      "Il Vincitore del Jackpot.",
      "un Imprenditore.",
    ];

    let cursor = gsap.to(".cursor", {
      opacity: 0,
      ease: "power2.inOut",
      repeat: -1,
    });
    let masterTl = gsap.timeline({ repeat: -1 }).pause();
    let boxTl = gsap.timeline();
    gsap.registerPlugin(TextPlugin);

    boxTl
      .to(".box", {
        duration: 1,
        width: "17vw",
        delay: 0.5,
        ease: "power4.inOut",
      })
      .from(".hi", { duration: 1, y: "7vw", ease: "power3.out" })
      .to(".box", {
        duration: 1,
        height: "7vw",
        ease: "elastic.out",
        onComplete: () => masterTl.play(),
      })
      .to(".box", {
        duration: 2,
        autoAlpha: 0.7,
        yoyo: true,
        repeat: -1,
        ease: "rough({ template: none.out, strength:  1, points: 20, taper: 'none', randomize: true, clamp: false})",
      });
    words.forEach((word) => {
      let tl = gsap.timeline({ repeat: 1, yoyo: true, repeatDelay: 1 });
      tl.to(".text", { duration: 1, text: word });
      masterTl.add(tl);
    });

    words;
    cursor;
  },
};
</script>

<style lang="scss" scoped>
section {
  font-family: "Playfair Display", serif;
  position: relative;
  height: 20rem;
  display: flex;
  align-items: center;
  justify-content: center;

  .one {
    background-image: url("../assets/img/backgroundred.jpg");
    background-size: cover;
  }
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
  color: var(--main1);
  text-shadow: 1px 1px 3px black;
  z-index: 1;
  font-size: 3em;
  font-weight: 400;
  overflow: hidden;
  position: relative;
}

h1 .hi {
  display: inline-block;
}

h1 .text {
  font-family: "Source Code Pro", sans-serif;
  font-weight: normal;
  margin-left: 1.2vw;
}
</style>