<template>
  <div class="container">
    <the-header>
      <template v-slot:title> home </template>
      <template v-slot:description>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores,
          accusamus?
        </p>
      </template>
      Content do header - menu
    </the-header>
  </div>
</template>

<script>
import TheHeader from "@/components/TheHeader.vue";
export default {
  name: "App",
  components: {
    TheHeader,
  },
  data() {
    return {};
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
