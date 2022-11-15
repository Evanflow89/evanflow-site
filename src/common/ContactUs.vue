<template>
  <section class="ContactUs d-flex align-items-center" id="Contatti">
    <div class="container contact">
      <div class="row">
        <div class="col-8 text-center">
          <h2>Contattaci</h2>
          <p class="pt-4">
            Inviaci la tua idea di grafica o affidati a noi. Avrai a
            disposizione un'ampia gamma di font, immagini e colori per
            customizzare completamente il tuo sito e renderlo il più unico
            possibile.
          </p>
          <p class="text-center pt-2 mail">
            <i class="fa-solid fa-arrow-right"></i
            ><i class="fa-solid fa-envelope"></i
            ><i class="fa-solid fa-arrow-left"></i>
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
  name: "ContactUs",
  mounted() {
    gsap.registerPlugin(ScrollTrigger);

    if (window.innerWidth < 576) {
      gsap.to(".contact", {
        scrollTrigger: {
          trigger: ".contact",
          start: "center center",
          end: "top center",
          once: true,
          scrub: 3,
        },
        x: 60,
        ease: "none",
        duration: 1,
      });
    } else if (window.innerWidth < 1000) {
      gsap.to(".contact", {
        scrollTrigger: {
          trigger: ".contact",
          start: "center center",
          end: "top center",
          once: true,
          scrub: 3,
        },
        x: 120,
        ease: "none",
        duration: 1,
      });
    } else {
      gsap.to(".contact", {
        scrollTrigger: {
          trigger: ".contact",
          start: "center center",
          end: "top center",
          once: true,
          scrub: 3,
        },
        x: 200,
        ease: "none",
        duration: 1,
      });
    }
  },
};
</script>

<style lang="scss" scoped>
.ContactUs {
  font-family: "Playfair Display", serif;
  height: 100vh;
  background-image: url("../assets/img/contactback.jpg");
  background-size: cover;
  color: white;
  font-size: 2rem;
  h2 {
    font-family: "Playfair Display", serif;
    font-size: 2.4rem;
  }
  .mail {
    display: flex;
    justify-content: center;
    gap: 1.25rem;
  }
  .fa-envelope:hover {
    color: var(--red);
  }
}
</style>