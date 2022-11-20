<template>
  <div id="Home">
    <header>
      <nav class="navbar fixed-top navbar-expand-lg navbar-dark">
        <div class="container-fluid">
          <a class="navbar-brand" href="#">Mishima Dev</a>
          <button
            class="navbar-toggler"
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#navbarNav"
            aria-controls="navbarNav"
            aria-expanded="false"
            aria-label="Toggle navigation"
          >
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ms-auto">
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="#Home"
                  >Home</a
                >
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#Noi">Perchè Noi</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#Contatti">Contattaci</a>
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </header>
    <section>
      <div class="bg one"></div>
      <h1 class="text-center">
        <span class="hi">Ciao, sono</span>
        <span class="text"></span>
        <span class="cursor">_</span>
      </h1>
    </section>
    <section>
      <div class="bg two"></div>
      <h1>un sito personalizzato</h1>
    </section>
    <section>
      <div class="bg three"></div>
      <h1>non ti serve veramente...</h1>
    </section>
  </div>
</template>

<script>
import { gsap } from "gsap";
import { TextPlugin } from "gsap/TextPlugin";
// import { ScrollTrigger } from "gsap/ScrollTrigger";

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
    //   gsap.registerPlugin(ScrollTrigger);

    //   gsap.utils.toArray(".bg").forEach((bg) => {
    //     ScrollTrigger.create({
    //       trigger: bg,
    //       start: "top top",
    //       end: "+=300px",
    //       pin: true,
    //       pinSpacing: false,
    //     });
    //   });
    // },
  },
};
</script>

<style lang="scss" scoped>
header {
  font-family: "Playfair Display", serif;
  font-size: 1.8rem;
  .navbar-brand {
    font-size: 2.3rem;
    font-family: "Megrim", cursive;
  }
}
section {
  font-family: "Playfair Display", serif;
  position: relative;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;

  .one {
    background-color: black;
  }
  .two {
    background-image: url("../assets/img/sfondo2.jpg");
  }
  .three {
    background-image: url("../assets/img/sfondo3.jpg");
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
  color: white;
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