<template>
  <div>
    <b-navbar toggleable="sm" type="dark" variant="dark">

      <b-navbar-brand href="#">Nuxt practice</b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item href="#">
            <nuxt-link class="nav-link" to='/'>Accueil</nuxt-link>
          </b-nav-item>
          <b-nav-item href="#">
            <nuxt-link class="nav-link" to='/commandes'>Commandes</nuxt-link>
          </b-nav-item>
        </b-navbar-nav>

      </b-collapse>
    </b-navbar>

    <div class="container">   
      <Nuxt />
    </div>
  </div>
</template>
<script>
  export default {

  }
</script>

<style>
</style>
