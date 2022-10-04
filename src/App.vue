<template>
  <div>
    {{ fullName }}<br>
    <h2>Todos en aberto</h2>
    <div v-for="todo in unCompletedTodos" :key="todo.id">
      {{todo.title}} - <span> {{ todo.completed }} </span>
    </div>
    <br>
    <h2> Todos completas</h2>
    <div v-for="todo in completedTodos" :key="todo.id">
      {{ todo.title }} <span>{{ todo.completed }}</span>
    </div>
    <br><br>
    <h2>Todos</h2>
    <div v-for="todo in todos" :key="todo.id">
      {{ todo.title }} <span>{{ todo.completed }}</span>
    </div>
    <br><br>
    <h2>Todos con checkbox</h2>
    <div v-for="todo in todos" :key="todo.id">
    <input type="checkbox" v-model="todo.completed">
    {{todo.title}}
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      user: {
        first_name: "Jon",
        last_name: "Snow",
      },
      todos: [
        {
          userId: 1,
          id: 1,
          title: "delectus aut autem",
          completed: false,
        },
        {
          userId: 1,
          id: 2,
          title: "quis ut nam facilis et officia qui",
          completed: false,
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
  computed: {
    fullName() {
      return `${this.user.first_name} ${this.user.last_name}`;
    },
    unCompletedTodos(){
      return this.todos.filter(todo => !todo.completed)
    },
    completedTodos(){
      return this.todos.filter(todo => todo.completed)
    }
  },
  methods: {
    click() {
      console.log(this.user);
    },
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
