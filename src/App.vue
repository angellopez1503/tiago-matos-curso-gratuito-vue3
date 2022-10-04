<template>
  <h1 :class="{ title: true, 'title-home': isHome }">Curso Vue3</h1>
  <p :class="pClass">
    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Asperiores,
    temporibus.
  </p>
  <p :style="styleClass">
    Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quidem ab eligendi
    dignissimos dolores illum debitis soluta perferendis mollitia sit illo?
  </p>
  <p :class="['btn',flag ? 'btn-success' : 'btn-danger',flag ? 'fw-bold' :'fw-normal', flag ? 'fs-1' : 'fs-6']">
    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aut dolorum vel
    atque tenetur tempore magni quae et ipsum dolores earum.
  </p>
  <div v-for="(obj, index) in todos" :key="obj.id" class="todos-item">
    <img v-if="obj.imgSrc" :src="obj.imgSrc" width="500" />
    {{ index + 1 }} - {{ obj.title }}
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      flag:true,
      isHome: true,
      classVar: "",
      pClass: ["text", "text-home"],
      styleClass: { color: "aqua", "background-color": "black" },
      todos: [
        {
          userId: 1,
          id: 1,
          title: "delectus aut autem",
          completed: false,
          imgSrc:
            "https://www.adslzone.net/app/uploads-adslzone.net/2019/04/borrar-fondo-imagen.jpg",
        },
        {
          userId: 1,
          id: 2,
          title: "quis ut nam facilis et officia qui",
          completed: false,
          imgSrc:
            "https://www.adslzone.net/app/uploads-adslzone.net/2019/04/borrar-fondo-imagen.jpg",
        },
        {
          userId: 1,
          id: 3,
          title: "fugiat veniam minus",
          completed: false,
        },
        {
          userId: 1,
          id: 4,
          title: "et porro tempora",
          completed: true,
        },
        {
          userId: 1,
          id: 5,
          title:
            "laboriosam mollitia et enim quasi adipisci quia provident illum",
          completed: false,
        },
      ],
    };
  },
};
</script>

<style scoped>
.title {
  font-size: 20px;
  color: blue;
}
.title-home {
  font-size: 40px;
  color: green;
}
.text {
  color: yellow;
}

.text-home {
  color: #42b983;
}
.todos-item {
  background: #000;
  margin: 0 0 5px 0;
  padding: 3px 6px;
  color: #fff;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
