<template>
  <footer>
    <div class="container pt-2">
      <div class="row d-flex align-items-center text-center">
        <div class="col-12 col-md-6">
          <h2>Mishima Dev</h2>
        </div>
        <div
          class="
            col-12 col-md-6
            d-flex
            justify-content-around
            align-items-center
          "
        >
          <i class="fa-solid fa-envelope"></i>
          <i class="fa-brands fa-facebook"></i>
          <i class="fa-brands fa-instagram"></i>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "BaseFooter",
};
</script>

<style lang="scss" scoped>
footer {
  background-image: url("../assets/img/footerback.jpg");
  background-size: cover;
  h2 {
    font-size: 2.5rem;
    font-family: "Megrim", cursive;
    color: white;
  }
  .fa-brands,
  .fa-solid {
    font-size: 2.2rem;
    color: white;
  }

  h2:hover,
  .fa-brands:hover,
  .fa-solid:hover {
    color: var(--red);
  }
}
</style>