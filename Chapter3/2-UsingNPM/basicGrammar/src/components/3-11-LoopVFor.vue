<template>
  <h1>{{ msg }}</h1>

  <div style="width: 200px">
    <ol>
      <li v-for="item in items">{{ item }}</li>
    </ol>
  </div>
</template>

<script>
import { reactive } from "vue";

export default {
  setup() {
    const items = reactive(["1번 아이템", "2번 아이템", "3번 아이템"]);
    // const items = reactive({ 1: '1qjs 객체', 2: '2번 객체', 3: '3번 객체' })

    return {
      items,
    };
  },

  props: {
    msg: String,
  },
};
</script>
