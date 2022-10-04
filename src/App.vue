<template>
  <div>
    <button @click.once="onClick">Enviar</button>
    <br />
    <div @mouseover="onMouseOver" @mouseout="onMouseOut">Mouse Over</div>
    <br><br>
    <form action="https://google.com" @submit.prevent="onSubmit">
      <input class="form-control" type="text" @keyup.enter="onKeyUp" ><br>
      <button type="submit" class="btn btn-primary">Enviar</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {};
  },
  methods: {
    onClick($evt) {
      console.log("click",$evt);
    },
    onMouseOver($evt) {
      console.log("mouse over",$evt);
    },
    onMouseOut($evt) {
      console.log("mouse out",$evt);
    },
    onSubmit(){
      console.log("submit");
    },
    onKeyUp($evt){
      console.log("onKeyUp",$evt);
    }
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
