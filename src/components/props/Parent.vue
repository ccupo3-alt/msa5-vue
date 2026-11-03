<script setup>
import { ref } from 'vue';
import Child from './Child.vue';

const user = ref({
  id: 1,
  name: '홍길동',
  age: 20
});
const str = ref('전달 문자열');
</script>

<template>
  <h2>Parent</h2>
  <Child :item="user" :str="str"/>
  <!-- item이라는 건 내가 지정하는 거임. 값만 가져오면 됨 -->
</template>

<style>

</style>