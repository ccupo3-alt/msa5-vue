<script setup>
import { ref } from 'vue';

const items = ref([
  {
    id: 1,
    kinds: '중식',
    food: '짜장면'
  },
  {
    id: 2,
    kinds: '한식',
    food: '비빔밥'
  },
  {
    id: 3,
    kinds: '일식',
    food: '돈까스'
  },
]);
// 이거 입력하면 Import 자동으로 됨
</script>

<template>
  <h2>List Rendering</h2>
  <div class="container">
    <div v-for="item in items" :key="item.id" class="card">
      <!-- 실무에서는 리스트성 값을 가져오면 대부분 변수명을 단수형으로 적음 -->
      <!-- key는 겹치지 않는 고유한 값이 담긴 걸로 설정하면 됨 -->
      <p>{{ item.kinds }}</p>
      <p>{{ item.food }}</p>
    </div>
  </div>
</template>

<style>

</style>
