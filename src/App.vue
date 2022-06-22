<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <ToDo></ToDo>
  <PWAPrompt></PWAPrompt>
  <!--  <HelloWorld msg="Hello World"></HelloWorld>-->
</template>

<script>
import ToDo from "./components/ToDo.vue";
import PWAPrompt from "@/components/PWAPrompt.vue";
// import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    ToDo,
    PWAPrompt,
    // HelloWorld,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
