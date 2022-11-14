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
      <h1>Forse</h1>
    </section>
    <section>
      <div class="bg two"></div>
      <h1>un sito personalizzato</h1>
    </section>
    <section>
      <div class="bg three"></div>
      <h1>non ti serve veramente...</h1>
    </section>
    <section>
      <div class="bg four"></div>
      <h1>Ma un sito web personalizzato</h1>
    </section>
    <section>
      <div class="bg five"></div>
      <h1>è bello, vero?</h1>
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

<style lang="scss" scoped>
header {
  font-family: "Playfair Display", serif;
  font-size: 1.8rem;
  .navbar-brand {
    font-size: 1.8rem;
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
    background-image: url("../assets/img/sfondo1.jpg");
  }
  .two {
    background-image: url("../assets/img/sfondo2.jpg");
  }
  .three {
    background-image: url("../assets/img/sfondo3.jpg");
  }
  .four {
    background-image: url("../assets/img/sfondo4.jpg");
  }
  .five {
    background-image: url("../assets/img/sfondo5.jpg");
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
  text-align: center;
  color: white;
  text-shadow: 1px 1px 3px black;
  z-index: 1;
  font-size: 3em;
  font-weight: 400;
}
</style>