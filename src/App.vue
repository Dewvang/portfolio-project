<template>
  <head>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Kode+Mono:wght@400..700&display=swap"
      rel="stylesheet"
    />
  </head>
  <body>
    <div class="container">
      <nav-component></nav-component>
      <head-component></head-component>
      <exp-component></exp-component>
    </div>
  </body>
</template>

<script>
import navComponent from "@/components/navComponent.vue";
import headComponent from "@/components/headComponent.vue";
import expComponent from "@/components/expComponent.vue";
export default {
  components: {
    navComponent,
    headComponent,
    expComponent,
  },
};
</script>

<style>
hr {
    background-color: #fff;
}

hr.hr-1 {
    border: 0;
    height: 1px;
    background-image: linear-gradient(to right,
            rgba(13, 18, 36, 1),
            rgba(164, 69, 178, 1),
            rgba(13, 18, 36, 1));
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Kode Mono", monospace;
  font-optical-sizing: auto;
  font-style: normal;
}
.container {
  width: 80%;
  height: auto;
  margin: 0 auto;
  justify-content: center;
  align-items: center;
}

body {
	background: #0d1224;
}

</style>
