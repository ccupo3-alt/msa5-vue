<script setup>
import { onBeforeMount, onMounted } from 'vue';


onBeforeMount(() => {
  alert('마운트 전에 실행됩니다.');
});
onMounted(() => {
  alert('마운트 후에 실행됩니다.');
})
// mount : 컴포넌트가 화면에 처음 생성되어 나타나는 과정
</script>

<template>
  <h2>Life Cycle</h2>
</template>

<style scoped>

</style>