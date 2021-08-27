<template>
  <div class="hero">
    <!-- desktop -->
    <div class="d-none d-md-block">
      <div class="row mt-4">
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h1><strong>Nikmati Menu </strong><br />Pilihan Terbaikmu</h1>
              <router-link class="btn btn-info" to="/foods">Pesan Sekarang</router-link>
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <img src="../assets/images/hero.png" width="100%" alt="" />
        </div>
      </div>
    </div>

    <!-- mobile -->
    <div class="d-sm-blok d-md-none">
      <div class="row mt-4">
        <div class="col-md-6 mb-2">
          <img src="../assets/images/hero.png" width="100%" alt="" />
        </div>
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h1><strong>Nikmati Menu </strong><br />Pilihan Terbaikmu</h1>
              <button class="btn btn-info">Pesan Sekarang</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style></style>
