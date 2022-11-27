<template>
  <header>
    <nav class="navbar fixed-top navbar-expand-lg navbar-dark">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">Mishima Dev</a>
        <button
          class="navbar-toggler"
          type="button"
          data-toggle="collapse"
          data-target="#navbarNav"
          aria-controls="navbarNav"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav ml-auto">
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
</template>

<script>
export default {
  name: "BaseHeader",
};
</script>

<style lang="scss">
header {
  font-family: "Playfair Display", serif;
  font-size: 1.8rem;
  .navbar-brand {
    font-size: 2.3rem;
    font-family: "Megrim", cursive;
  }
}
</style>