<script setup>
import { ref, watch } from 'vue';

const test = ref('');
const testErrorMsg = ref('');
const testColor = ref('');

// watchers : 데이터의 변화를 감시하는 함수
// (1. 감시하고 싶은 대상, 2. 실행시키고 싶은 처리를 콜백함수로 작성)
watch(test,(val) => {
  const pattern = /^[a-zA-Z]+$/;
  // ^~$는 처음부터 끝까지라는 뜻
  if(val === ''){
    testErrorMsg.value = '';
  } else if (pattern.test(val)){
    // test라는 메소드가 있음. 검증하고 싶은 값을 파라미터로 입력, 부합하면 true 부합하지 않으면 false
    testErrorMsg.value = 'O';
    testColor.value = "color: green;"
  } else{
    testErrorMsg.value = 'X';
    testColor.value = "color: red;"
  }
});

</script>

<template>
  <h2>Watchers : 감시자</h2>

  <input type="text" v-model="test">
  <p :style="testColor">{{ testErrorMsg }}</p>
</template>

<style>

</style>