<script setup>
import DataBinding from './components/DataBinding.vue';
import ConditionalRendering from './components/ConditionalRendering.vue';
import ListRendering from './components/ListRendering.vue';
import Ex from './components/Ex.vue';
import ClaudeTab from './components/ClaudeTab.vue';
import Watchers from './components/Watchers.vue';
import Parent from './components/props/Parent.vue';
import SlotParent from './components/slot/SlotParent.vue';
import CEParent from './components/componentEvent/CEParent.vue';
import LifeCycle from './components/LifeCycle.vue';
import CardList from './components/CardList.vue';
</script>

<template>
  <h1>APP Component</h1>
  <!-- <DataBinding></DataBinding> -->
  <!-- <DataBinding/>로 적어도 됨 -->
  <!-- <ConditionalRendering/> -->
  <!-- <ListRendering/> -->
  <!-- 이거 입력하면 import 자동으로 됨 -->
  <!-- <h3>TabUI</h3> -->
  <!-- <Ex/> -->
  <!-- <ClaudeTab/> -->
  <!-- <Watchers/> -->
  <!-- <Parent/> -->
  <!-- <SlotParent/> -->
  <!-- <CEParent/> -->
  <!-- <LifeCycle/> -->
  <CardList/>
</template>

<style>

</style>
<!-- components 안 vue 파일 이름은 대문자로 시작하는 파스칼 기법으로 작성 -->