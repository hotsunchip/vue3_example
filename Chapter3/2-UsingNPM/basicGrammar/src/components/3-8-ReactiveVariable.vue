<template>
  <h1>{{ msg }}</h1>

  <p>줄임말과 원래말을 입력하세요.</p>
  <input type="text" v-bind:value="abbr" />
  <!-- v-model은 반드시 value 속성과 결합됨 -->
  <input type="text" v-model="normal" />
  <hr />
  <abbr v-bind:title="normal">{{ abbr }}</abbr>
</template>

<script>
import { ref } from "vue";

export default {
  // Composition API
  setup() {
    const abbr = ref("DOPT");
    const normal = ref("Dong Project Team");
    return {
      abbr,
      normal,
    };
  },

  props: {
    msg: String,
  },
};
</script>