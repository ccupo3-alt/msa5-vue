<script setup>
import { ref } from 'vue';

const num = ref(0);
const flg = ref(true);
</script>

<template>
  <input type="number" v-model="num">
  <p v-if="num === 0">0입니다</p>
  <p v-else-if="num % 2 === 0">짝수입니다</p>
  <p v-else>홀수입니다</p>
  <hr>
  <button :class="{'btn-toggle': flg === false}" @click="flg = !flg">토글</button>
  <p v-if="flg">v-if</p>
  <!-- 값이 0이거나 ''(빈 문자열), null, undefinded면 false로 처리됨 -->
  <p v-show="flg">v-show</p>
</template>

<style>
.btn-toggle {
  background-color: aqua;
}
</style>