<template>
  <nav>
    <ul>
        <li><RouterLink to="/">Acceuil</RouterLink></li>
        <li><RouterLink to ="/demo"> Les demos</RouterLink></li>
    </ul>
  </nav>
</template>

<script lang="ts">
export default {
  name: "Test",
  created() {},
  data() {
    return {};
  },
  props: {},
  methods: {},
};
</script>

<style scoped>

nav{
    background-color: lightsalmon;
    height: 5vh;
    
}
ul{
    display: flex;
    align-items: center;
}
li
{
    list-style: none;
    margin: 0 1%;
}
a{
    text-decoration: none;
    font-size: 2rem;
    color:black;
}
a:hover{
    color:green;
}
a:visited{
    color:white;
    font-size: 2rem;
}
</style>