<template>
  <h1>{{ msg }}</h1>

  <div id="date">
    {{ date }}
  </div>
  <div id="date2">
    {{ date2 }}
  </div>
</template>

<script>
export default {
  // Composition API
  setup() {
    const date = Date().toString();
    return {
      date, // ES6 단축 속성: 객체의 키 값과 변수명이 동일할 경우 변수명을 작성하지 않아도 됨
    };
  },

  // Options API
  data() {
    return {
      date2: Date().toString(),
    };
  },

  props: {
    msg: String,
  },
};
</script>