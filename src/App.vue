<template>
  <splitpanes class="default-theme">
    <pane>
      <splitpanes class="default-theme" horizontal="horizontal">
        <pane min-size="15"
          >2<br /><em class="specs">I have a min height of 15%</em></pane
        >
        <pane>3</pane>
        <pane>4</pane>
      </splitpanes>
    </pane>
    <pane>5</pane>
  </splitpanes>
  <p>
    Documentation @<a href="https://antoniandre.github.io/splitpanes"
      >antoniandre.github.io/splitpanes</a
    >
  </p>

  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Welcome to Your Vue.js + TypeScript App" />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import HelloWorld from "./components/HelloWorld.vue";
import { Splitpanes, Pane } from "splitpanes";
import "splitpanes/dist/splitpanes.css";

export default defineComponent({
  name: "App",
  components: { Splitpanes, Pane, HelloWorld },
});
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

.splitpanes__pane {
  box-shadow: 0 0 3px rgba(0, 0, 0, 0.2) inset;
  justify-content: center;
  align-items: center;
  display: flex;
  position: relative;
}

em.specs {
  font-size: 0.2em;
  line-height: 1;
  position: absolute;
  color: #bbb;
  bottom: 0.5em;
  left: 0;
  right: 0;
  text-align: center;
}

html,
body,
#app {
  height: 100%;
  margin: 0;
}
body {
  font-family: Helvetica, Arial, sans-serif;
  color: rgba(255, 255, 255, 0.6);
  font-size: 5em;
}

p {
  position: absolute;
  bottom: 5px;
  right: 5px;
  color: #666;
  z-index: 10;
  font-size: 12px;
  a {
    color: inherit;
  }
}
</style>
