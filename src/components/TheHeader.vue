<template>
  <header class="header">Header</header>
  
</template>
<script>
export default {


  mounted(){
    console.log("sas")
    window.addEventListener("resize",this.resize)
  },

  beforeUnmount(){
    console.log("beforeUnmount");
    window.removeEventListener("resize",this.resize)
  },
  unmounted(){
    console.log("unmounted");
  },
  methods:{
    resize($evt){
      console.log($evt)
    }
  }
};
</script>
<style scoped>
 .header{
  background:#000 ;
  color: #fff;
 }
</style>
