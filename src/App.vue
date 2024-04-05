<template>
  <body>
    <div class="container">
      <router-view></router-view>
    </div>
  </body>
</template>

<script>
export default {};
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
  background-image: linear-gradient(to right, #6a11cb 0%, #2575fc 100%);
}
</style>
