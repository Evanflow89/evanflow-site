<template>
  <section>
    <div class="container_custom pt-5 pb-5">
      <div class="row d-flex align-items-center justify-content-center">
        <div class="col-12 col-md-4 pt-5 text-center">
          <h2>Crea il tuo sito</h2>
        </div>
        <div class="col-12 col-md-6 pt-5">
          <img
            class="img-fluid teamImage"
            src="../assets/img/section1.jpg"
            alt="persone al pc"
          />
        </div>
      </div>

      <!-- ################ SECONDA PARTE ################ -->
      <div class="row d-flex align-items-center justify-content-center pt-5">
        <div
          class="
            col-12 col-md-6
            pt-5
            d-flex
            justify-content-center
            order-1 order-md-6
          "
        >
          <img
            class="teamImage img-fluid"
            src="../assets/img/section2.jpg"
            alt="ricerca google"
          />
        </div>
        <div class="col-12 col-md-4 pt-5 order-6 order-md-1 text-center">
          <h2>Fatti trovare</h2>
        </div>
      </div>
      <!-- ################ TERZA PARTE ################ -->
      <div class="row d-flex align-items-center justify-content-center">
        <div class="col-12 col-md-10 pt-5">
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate
            omnis alias doloremque impedit labore placeat debitis culpa dolorum
            quas? At ratione eveniet laboriosam. Delectus numquam fuga, magnam
            in impedit dolorum.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "MiddleMain",
};
</script>

<style lang="scss" scoped>
section {
  background-color: white;
  color: var(--text);
}

h2 {
  text-transform: uppercase;
  color: var(--textgray);
  font-size: 5rem;
  position: relative;
}

h2::after {
  content: "CREA IL TUO SITO";
  color: var(--text);
  position: absolute;
  left: 0;
  top: 60px;
  bottom: 0;
  right: 0;
  font-size: 3rem;
}

.container_custom {
  width: 100vw;
}
</style>