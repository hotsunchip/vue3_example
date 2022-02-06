<template>
  <h1>{{ msg }}</h1>

  <p>{{ counter + counter2 }}</p>
  <button @click="counter++">클릭하면 숫자가 올라갑니다.</button>
  <button @click="onClick">클릭하면 숫자가 올라갑니다.</button>
</template>

<script>
import { ref } from "vue";

export default {
  props: {
    msg: String,
  },

  data() {
    return {
      counter2: 0,
    };
  },

  setup() {
    let counter = ref(0);

    const onClick = (evt) => {
      if (evt) {
        evt.preventDefault();
        counter.value++; // setup 함수에서 ref 함수를 통해 선언된 변수는 프록시 객체로 변환됨
      }
    };
    return {
      counter,
      onClick, // 컴포지션 디렉티브에서는 함수 선언도 return 문을 통해 반환해야 템플릿에서 사용 가능
    };
  },

  methods: {
    // Options API에서 함수를 만들기 위해서는 methods라는 옵션에 선언하면 됨
    onClick2: function (evt) {
      if (evt) {
        evt.preventDefault();
      }
      this.counter2++;
    },
  },
};
</script>
