<template>
  <div class="home">
    <navbar />
    <div class="container">
      <hero />
      <div class="row mt-5">
        <div class="col">
          <h2><strong>Menu</strong> Terlaris</h2>
        </div>
        <div class="col">
          <router-link class="btn btn-info float-right" to="/foods">
            <b-icon-eye></b-icon-eye> Lihat Semua Menu
          </router-link>
        </div>
      </div>
      <div class="row mb-4">
        <div class="col-md-4 mt-4" v-for="product in products" :key="product.id">
          <card-product :product="product"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import Hero from "../components/Hero.vue";
import CardProduct from "../components/CardProduct.vue";
import axios from "axios";

export default {
  name: "Home",
  components: {
    Navbar,
    Hero,
    CardProduct,
  },
  // wadah data (parameter)
  data() {
    return {
      products: []
    }
  },
  // mengambil data dari mounted
  methods: {
    setProducts(data) {
      this.products = data
    },
  },
  // mounted mengambil data dari API dengan endpoint (http://localhost:3000/best-products)
  mounted() {
    axios
      .get("http://localhost:3000/best-products")
      .then((response) => this.setProducts(response.data))
        // kenapa response.data karena object berada di respon bagian data (jika di inspect)
      .catch((error) =>console.log("Gagal = ", error))
        // respon kalo gagal
  },
};
</script>
