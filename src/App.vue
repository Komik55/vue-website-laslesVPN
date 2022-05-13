<template>
  <div class="mx-auto wrapper py-9">
    <about />
    <features />
  </div>
</template>

<script>
import "./assets/tailwind.css";
import About from "./components/about.vue";
import Features from "./components/features.vue";

export default {
  name: "App",
  components: {
    About,
    Features,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-family: Rubik;
  font-size: 16px;
  width: 100%;
}
h1,
h2 {
  color: #0b132a;
}
#app {
  height: 100vh;
  background-color: #fff;
}
.wrapper {
  width: 85%;
}
@media screen and (max-width: 520px) {
  .wrapper {
    width: 90%;
  }
}
</style>
