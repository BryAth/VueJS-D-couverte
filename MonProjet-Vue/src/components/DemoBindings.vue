<template>
    <div class="demo"> 
        <h1>Demo des bindings</h1>
    
        <div class="chapitre"> 
        Binding oneWay
            <h2>{{lastname}}</h2>
            <h2>{{firstname}}</h2>
            <h2>Vous avez {{age}} ans</h2>
        </div>

            <div class="chapitre">
                <h3>Property binding two way</h3>
                <p> Vous avez {{age}} ans </p>
                <input type="text" v-model="firstname"> 
            </div>
                
                <div class="chapitre">
                    <h3> Event Binding</h3>
                    <p>{{message}}</p>
                    <button @click="afficherBonjour('fr')">En francais</button>
                    <button @click="afficherBonjour('en')">En anglais</button>
                    <button @click="afficherBonjour('it')">En italien</button>
                </div>
                    <div class="chapitre">
                    <h3> Attribute Binding </h3>
                    <div :id="monId">Binding de l'attribut Id </div>
                    <button :disabled="isInactive"> Click</button>
                    
                    </div>
    </div>
    
</template>

<script lang="ts">
import  { defineComponent } from "vue";
export default defineComponent({
  name: "Test",
  created() {},
  data() {
    return {
        lastname : 'Lequeux',
        firstname : 'Bryan',
        age : 26,
        message : 'En attente d\'une salutation',
        monId :     "pouet",
        isInactive : true
    };
  },
  
  methods: {
    afficherBonjour(langue: string) {
        switch(langue){
            case "fr" : 
        this.message = "Bonjour  " + this.firstname
        break;
        case"en" :
        this.message = "Hello " + this.firstname
        break;
        case "it" : 
        this.message = "Ciao "  + this.firstname
        break;
        default : 
        this.message = "Je ne comprends pas votre langue"
        break;
        }
        
    }
  },
});
</script>

<style scoped>
.chapitre{
background-color: lightsalmon;
width:90%;
padding: 1%;
margin-bottom: 15px;
}</style>