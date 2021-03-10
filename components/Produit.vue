<template >
  <div class="card text-white bg-dark mb-3" style="width: 18rem;">
    <div class="card-body">
      <h5 class="card-title">{{ nom }}</h5>
      <p class="card-text">Prix : {{ prix }}</p>
      <hr v-if="role == 'commander'">
      <button v-if="role == 'commander'" @click="$emit('commande', nom, prix)" class="btn btn-success">Commander</button>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Produit",
    props: ["nom", "prix", "role"]
  }
</script>

<style >
  
</style>