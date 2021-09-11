<template>
  <div id="app">
    <TitleBar />
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import TitleBar from "./components/TitleBar.vue";

export default {
  name: "App",
  components: {
    TitleBar,
    HelloWorld,
  },
};
</script>

    <style>
body,
html {
  margin: 0px;
  padding: 0px;
  overflow: hidden;
  height: 100%;
}
#app {
  text-align: center;
  margin: 0px;
  padding: 0px;
  height: 100%;
  overflow: hidden;
  box-sizing: border-box;
  border: 1px solid #f5222d;
  display: flex;
  flex-direction: column;
}
</style>
