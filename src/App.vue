<template>
  <div class="container">
    <the-header v-if="showHeader"></the-header>
    <h1>Hello World</h1>
   {{name}}<br>
   <input type="text" v-model="name">
   <button @click="showHeader = !showHeader" >Activar / Desactivar</button>
  </div>
</template>

<script>
  import TheHeader from '@/components/TheHeader.vue'
export default {
  name: "App",
  components: {
    TheHeader
  },
  data() {
    return { 
      name:"Angel",
      showHeader:true
    };
  },
    

    // beforeUpdate(){
    //     console.log("beforeUpdate",this.name)
    // },

    // updated(){
    //   console.log("updated",this.name)
    // }



  // beforeCreate(){
  //  console.log("beforeCreate")
  //  console.log('Estado : ',this.name);
  //  console.log("DOM",this.$el)
  // },
  // created(){
  //   console.log("created");
  //   console.log('Estado : ',this.name);
  //   console.log("DOM",this.$el)
  // },
  // beforeMount(){
  //   console.log("beforeAmount");
  //   console.log('Estado : ',this.name);
  //   console.log("DOM",this.$el)
  // },
  // mounted(){
  //   console.log("mounted");
  //   console.log('Estado : ',this.name);
  //   console.log("DOM",this.$el)
  // },
  // beforeUnmounted(){
  //   console.log("beforeUnmounted");
  // },
  // unmounted(){
  //   console.log("unmounted");
  // }
  
  
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
