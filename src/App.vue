<script setup>
import { ref } from 'vue';

const count = ref(0);
</script>

<template>
  <div @click="count++" class="btn-cnt">count is {{ count }}</div>
  <button @click="count = 0">Count Reset</button>
</template>

<style>
.btn-cnt{
  width: 100px;
  height: 100px;
  background-color: aliceblue;
}
</style>
// 전체적으로 들어가는 css는 style.css에 입력하면 됨