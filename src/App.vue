<template>
  <div></div>
  <input type="text" v-model="name" />
  <br />
  {{ name }}
  <br />
  <br>
  <div>
    <select name="" id="" v-model="sports">
      <option value="futbol">Futbol</option>
      <option value="skate">Skate</option>
      <option value="tenis">Tenis</option></select
    ><br />
    {{ sports }}
  </div>
  <br /><br />
  <div>
    <label for="">News letter</label><br />
    <input type="radio" value="Sim" v-model="newsletter" />Sim
    <input type="radio" value="Ñao" v-model="newsletter" />Ñao
    <br>
    {{newsletter}}
  </div>
<br>
<br>
<div>
  <label for="">Contrato</label><br />
  <input type="checkbox" v-model="contract" />Acpeta nuestros terminos
  
  <br>
  {{contract}}
</div>
<br>
<br>
<div>
  <label for="">Varios checkbox</label><br />
  <input type="checkbox" value="Azul" v-model="colors" />Azul
  <input type="checkbox" value="Amarillo" v-model="colors" />Amarillo
  <br>
  {{colors}}
</div>

</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      name: "Angel",
      sports: "futbol",
      newsletter:'',
      contract:true,
      colors:[]
    };
  },
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
