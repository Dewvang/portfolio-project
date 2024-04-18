<template>

  <head>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Kode+Mono:wght@400..700&display=swap" rel="stylesheet" />
  </head>

  <body>
    <div class="container">
      <nav-component></nav-component>
      <head-component></head-component>
      <exp-component></exp-component>
      <education-component></education-component>
      <skills-component></skills-component>
      <project-component></project-component>
      <footer-component></footer-component>
    </div>
    <button id="back-to-top-btn" @click="scrollToTop">
      ↑
    </button>
  </body>
</template>

<script>
import navComponent from "@/components/navComponent.vue";
import headComponent from "@/components/headComponent.vue";
import expComponent from "@/components/expComponent.vue";
import educationComponent from "@/components/educationComponent.vue";
import skillsComponent from "@/components/skillsComponent.vue";
import projectComponent from "@/components/projectComponent.vue";
import footerComponent from "@/components/footerComponent.vue";
export default {
  components: {
    navComponent,
    headComponent,
    expComponent,
    educationComponent,
    skillsComponent,
    projectComponent,
    footerComponent
  },
  methods: {
    scrollToTop() {
      window.scrollTo({
        top: 0,
        behavior: "smooth"
      });
    }
  }
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

#back-to-top-btn {
  position: fixed;
  bottom: 20px;
  right: 20px;
  padding: 10px;
  background-color: rgba(13, 18, 36, 1);
  color: #fff;
  width: 40px;
  border-radius: 100%;
  cursor: pointer;
  z-index: 999;
}

#back-to-top-btn:hover {
  transform: scale(1.1);
    transition: transform 0.3s ease;
}
</style>
