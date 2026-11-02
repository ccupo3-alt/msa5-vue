<script setup>
import { ref } from 'vue';

const count = ref(0);
const bgColor = ref('');
const email = ref('');

// 
const toggleBgColor = ()=>{
  if(bgColor.value === ''){
    bgColor.value = 'bg-red';
  } else {
    bgColor.value = '';
  }
}
</script>

<template>
  <div @click="count++" class="btn-cnt" :class="bgColor">count is {{ count }}</div>
  <button @click="count = 0">Count Reset</button>
  <button @click="count--">Count Down</button>
  <button @click="bgColor = 'bg-red'">red</button>
  <button @click="bgColor = ''">aliceblue</button>
  <button @click="toggleBgColor()">Toggle</button>
  <br><br>
  <input type="text" name="email" id="email" :v-model="email">
  {{ email }}
</template>

<style>
.btn-cnt{
  width: 100px;
  height: 100px;
  background-color: aliceblue;
}
.bg-red{
  background-color: red;
}
/* bg-red를 아래에 적어야 함 왜? 가장 아래에 있는 코드가 덮어써버림*/
</style>
// 전체적으로 들어가는 css는 style.css에 입력하면 됨