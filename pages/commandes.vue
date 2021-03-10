<template >
  <div>
    <h1 class="display-1">Commander</h1>
    
    <h2 class="mt-3">Produits disponibles</h2>

    <div class="card-deck">
      <Produit 
        v-for="produit in produits" 
        :key="produit.nom"
        :nom="produit.nom"
        :prix="produit.prix"
        v-on:commande="ajouterProduit"
        role="commander"
      />
    </div>

    <h2 class="mt-3">Produits Commandés</h2>
    <div class="card-deck">
      <Produit 
        v-for="produit in commandes" 
        :key="produit.nom"
        :nom="produit.nom"
        :prix="produit.prix"
        role="affichage"
      />
    </div>

  </div>
</template>

<script>
  import Produit from '@/components/Produit.vue'

  export default {
    components: {
      Produit
    },
    data() {
      return {
        produits: [
          { nom: 'Pizza', prix: 3.0 },
          { nom: 'Frites', prix: 2.0 },
          { nom: 'Burger', prix: 2.5 }
        ],
        commandes: [
         { nom: 'Frites', prix: 2.0 }
        ]
      }
    },
    methods:{
      ajouterProduit(nom, prix) {
        this.commandes.push({nom, prix})
      }
    }
    
  }
</script>

<style scoped>
  
</style>