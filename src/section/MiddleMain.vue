<template>
  <section>
    <div class="container pt-5 pb-5">
      <div class="row d-flex align-items-center justify-content-center">
        <div class="col-12 col-md-5 pt-5">
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate
            omnis alias doloremque impedit labore placeat debitis culpa dolorum
            quas? At ratione eveniet laboriosam. Delectus numquam fuga, magnam
            in impedit dolorum.
          </p>
        </div>
        <div class="col-12 col-md-5 pt-5">
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
            col-12 col-md-5
            pt-5
            d-flex
            justify-content-center
            order-1 order-md-6
          "
        >
          <img
            class="teamImage"
            src="../assets/img/section2.jpg"
            alt="persone al pc"
          />
        </div>
        <div class="col-12 col-md-5 pt-5 order-6 order-md-1">
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
.teamImage {
  border-radius: 15px;
  overflow: hidden;
  max-height: 25rem;
  height: 100%;
}
</style>