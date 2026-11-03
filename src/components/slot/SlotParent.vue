<script setup>
import SlotChild from './SlotChild.vue';

</script>

<template>
  <h2>Slot Parent</h2>
  <SlotChild>부모에서 보낸 버튼</SlotChild>
  <SlotChild>전송</SlotChild>
  <SlotChild></SlotChild>
  <!-- 아무 내용도 안 넣으면 SlotChild에 있는 슬롯 안 내용이 표시됨 -->
</template>

<style scoped>

</style>