<template>
  <nav-component></nav-component>
  <header>
    <div>
      <h1>Hello, This is ABU SAID , I'm a Professional Software Developer.</h1>
    </div>
    <div>
      <img :src="require('@/assets/Profile.png')" alt="">
    </div>
  </header>
</template>

<script>
import navComponent from "@/components/navComponent.vue";
export default {
  components: { navComponent },
};
</script>

<style scoped>
  
</style>