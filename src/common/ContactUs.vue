<template>
  <section class="ContactUs d-flex align-items-center" id="Contatti">
    <div class="container contact">
      <div class="row d-flex justify-content-center">
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
export default {
  name: "ContactUs",
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
  @media screen and (max-width: 1000px) {
    .row {
      justify-content: center;
    }
  }
}
</style>