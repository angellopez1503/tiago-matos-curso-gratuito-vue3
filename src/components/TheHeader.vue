<template>
  <header class="header">
    <h1 class="title" v-if="$slots.title">
      <slot name="title"></slot>
    </h1>
    <div class="description">
      <slot name="description"></slot>
    </div>
    <div class="content">
      <slot></slot>
    </div>
  </header>
</template>
<script>
export default {

  mounted(){
    console.log(this.$slots.description)
  }

};
</script>
<style scoped>
.header {
  background: #000;
  color: #fff;
}
</style>
