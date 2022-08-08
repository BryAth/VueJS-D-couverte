<template>
    <div class="demo">
        <h2> Démo des directives </h2>
    </div>
    <div class="chapitre">
    <h3>Directives conditionelles</h3>
    <button @click="modeNuit = !modeNuit">🌜/☀️</button>
    <div v-if="modeNuit" class="nuit">Nuit</div>
    <div v-else class="jour">Jour</div>
    </div>

    <div class="chapitre">
    <h3>  Directive de boucle</h3>
    <div>Avec tableau simple</div>
    <ul>
    <li v-for="(article,index) in listeCourse">{{index}}-{{article}}</li>

    
    </ul>
    <div> Avec tableau d'objet</div>
        <div v-for="formateurs in formateurs">
    <img :src="formateurs.image">
                <div>{{formateurs.firstname}} {{formateurs.lastname}}</div>
                <div>{{formateurs.birthday}}</div>
        </div>
    </div>
</template>

<script lang="ts">
export default {
  name: "Test",
  created() {},
  data() {
    return {
        modeNuit : false,
        listeCourse : ["Patate","Poulet","Salade","Moutarde"],
        
        
        
        formateurs : [{
            firstname : "Aude",lastname : "Beurive",
            birthday : "16/10/1989",image : "../src/assets/img/street-g85794b93b_1920.jpg"},
            {
            firstname : "Aurélien",lastname : "Strimelle",birthday : "1/11/1989"
            },
            {firstname : "Khun",lastname : "Ly",birthday : "06/05/1982"}
            ]

    };
},
props: {},
methods: {},
};
</script>

<style scoped>
.chapitre{
background-color: lightsalmon;
width:90%;
padding: 1%;
margin-bottom: 15px;
}

.nuit{
    background-color: black;
    width: 150px;
    height: 80px;
    color:white;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: 600;
    margin: auto;
}

.jour{
    background-color: skyblue;
    width: 150px;
    height: 80px;
    color:white;
    display: flex;
    align-items: center;
    font-weight: 600;
    justify-content: center;
    margin: auto;
}
img{
width:450px;
height: 450px;
}
</style>