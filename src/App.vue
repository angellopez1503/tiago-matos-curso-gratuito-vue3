<template>
  <div class="container">
    <BaseAlert :variant="variant" :text="text" @close="onClose" v-if="showAlert" />
  </div>
</template>

<script>
import BaseAlert from "./components/BaseAlert.vue";
export default {
  name: "App",
  components: {
    BaseAlert
},
  data() {
    return {
      showAlert:true,
      text:'El formulario fue enviado',
      variant:'success'
    };
  },
  methods:{
    onClose(){
      console.log("on close")
      this.showAlert = false
    }
  }
};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
