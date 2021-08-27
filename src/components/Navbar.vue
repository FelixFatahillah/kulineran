<template>
  <div>
      <b-navbar toggleable="lg" type="light" variant="transpararent">
        <div class="container">
            <b-navbar-brand href="#">Marung</b-navbar-brand>

            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

            <b-collapse id="nav-collapse" is-nav>
            <b-navbar-nav>
              <b-nav-item>
                <router-link class="nav-link" to="/">Home</router-link>
              </b-nav-item>
              <b-nav-item>
                <router-link class="nav-link" to="/foods">Foods</router-link>
              </b-nav-item>
            </b-navbar-nav>

            <b-navbar-nav class="ml-auto">
              <b-nav-item>
                <router-link class="nav-link" to="/keranjang">
                  <b-icon-bag></b-icon-bag>
                  <span class="badge badge-info ml-2">0</span>
                </router-link>
              </b-nav-item>
            </b-navbar-nav>
          </b-collapse>
        </div>  
      </b-navbar>
    </div>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style>
</style>