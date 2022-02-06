<script setup>
// 여기에 components 추가
import HelloWorld from "./components/HelloWorld.vue";
import Example_3_7 from "./components/3-7-DeclarativeRendering.vue";
import Example_3_8 from "./components/3-8-ReactiveVariable.vue";
import Example_3_9 from "./components/3-9-EventListenerExample.vue";
import Example_3_10 from "./components/3-10-Conditional.vue";
import Example_3_11 from "./components/3-11-LoopVFor.vue";
</script>

<template>
  <!-- img alt="Vue logo" src="./assets/logo.png" /-->
  <!--HelloWorld msg="Hello Vue 3 + Vite" / -->
  <!-- <Example_3_7 msg="3-7-DeclarativeRendering.vue" /> -->
  <!-- <Example_3_8 msg="3-8-ReactiveVariable.vue" /> -->
  <!-- <Example_3_9 msg="3-9-EventListenerExample.vue" /> -->
  <!-- <Example_3_10 msg="3-10-Conditional.vue" /> -->
  <Example_3_11 msg="3-11-LoopVFor.vue" />
</template>

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
