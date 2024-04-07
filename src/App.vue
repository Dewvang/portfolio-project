<template>
  <body>
    <div class="container">
      <nav-component></nav-component>
      <head-component></head-component>
      <!-- <router-view></router-view> -->
    </div>
  </body>
</template>

<script>
import navComponent from "@/components/navComponent.vue";
import headComponent from "@/components/headComponent.vue";
export default {
    components: { 
      navComponent, 
      headComponent
    },
    
};

</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}
.container {
  width: 80%;
  height: auto;
  margin: 0 auto;
  justify-content: center;
  align-items: center;
}

body {
  background-color: black;
}
</style>
