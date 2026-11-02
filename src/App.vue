<script setup>
import DataBinding from './components/DataBinding.vue';
import ConditionalRendering from './components/ConditionalRendering.vue';
import ListRendering from './components/ListRendering.vue';
import Ex from './components/Ex.vue';
</script>

<template>
  <h1>APP Component</h1>
  <!-- <DataBinding></DataBinding> -->
  <!-- <DataBinding/>로 적어도 됨 -->
  <!-- <ConditionalRendering/> -->
  <!-- <ListRendering/> -->
  <!-- 이거 입력하면 import 자동으로 됨 -->
  <h3>TabUI</h3>
  <Ex/>
</template>

<style>

</style>
<!-- components 안 vue 파일 이름은 대문자로 시작하는 파스칼 기법으로 작성 -->