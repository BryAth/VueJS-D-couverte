<template>
  <div>Les démos vont se trouver ici</div>
  <DemoBindings> </DemoBindings>
  <DemoDirective></DemoDirective>
</template>

<script lang="ts">
import DemoBindings from '../components/DemoBindings.vue'
import DemoDirective from '@/components/DemoDirective.vue';
export default {
  name: "Test",
  created() {},
  data() {
    return {};
  },
  props: {},
  methods: {},
  components:{
    DemoBindings,
    DemoDirective
  }
};
</script>

<style scoped>

.demo{
    width: 80%;
    background-color: grey;
    margin: auto;
    padding: 2%;
}



</style>