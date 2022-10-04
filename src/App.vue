<template>
  <div class="container">
    <br>
    <input 
      type="text"
      v-model="name"
    >
    <br>
    {{ name }}
    <br><br>
    <input 
      type="text"
      v-model="user.first_name"
      ><br>
    <input 
      type="text"
      v-model="user.last_name"
      ><br>
      {{ user.first_name }} {{user.last_name}}

    <br><br><br>
    <select v-model="pageCount">
      <option value="5">5</option>
      <option value="10">10</option>
      <option value="15">15</option>
    </select><br>

    {{pageCount}}

  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
     name:'',
     pageCount:5,
     user:{
      first_name:'',
      last_name:''
     }
    };
  },
  watch:{
    name(vl){
      // console.log(newValue,oldValue);
      if(vl.length >=3){
      this.saveUserName()
      }
    },
    pageCount(){
      this.changePage()
    },
    user:{
      handler(item){
        console.log('User alterado');
        if(item.first_name.length>3){
          console.log("error");
          
        }
      },
      deep:true
    }
  },
  methods:{
    saveUserName(){
        console.log(this.name);
      
    },
    changePage(){
      console.log('Ajax changePage')
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
