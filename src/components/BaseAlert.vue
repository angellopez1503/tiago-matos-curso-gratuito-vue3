<template>
  <div :class="baseClass">
    {{ text }}

    <button @click="onClick" class="btn btn-primary">x</button>
  </div>
</template>
<script>
export default {
  props: {
    variant: {
      type: String,
      default: "",
    },
    text: {
      type: String,
      default: "",
    },
  },
  computed: {
    baseClass() {
      return ["alert", this.variant ? `alert-${this.variant}` : ""];
    },
  },
  methods:{
    onClick(){
        this.$emit("close")
        console.log("click")
    }
  }
};
</script>
<style scoped>
.alert {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 5px;
  border-radius: 6px;
  color: gray;
  background: #ddd;
}

.alert-success {
  background: #42b983;
  color: #fff;
}
.alert-danger {
  background: red;
  color: #fff;
}
</style>
