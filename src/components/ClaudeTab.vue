<script setup>
import { ref } from 'vue';

const tabs = [
  { key: 'pro', label: '프로필', text: '프로필 페이지입니다.' },
  { key: 'set', label: '설정', text: '설정 페이지입니다.' },
  { key: 'noti', label: '게시판', text: '게시판 페이지입니다.' },
];

const current = ref('pro'); // 처음부터 프로필 탭 선택
</script>

<template>
  <div class="btn">
    <button
      v-for="tab in tabs"
      :key="tab.key"
      :class="{ active: current === tab.key }"
      @click="current = tab.key"
    >
      {{ tab.label }}
    </button>
  </div>

  <p class="content">{{ tabs.find(t => t.key === current).text }}</p>
</template>

<style scoped>
.btn {
  display: flex;
  margin: 20px auto;
  border-radius: 10px;
  overflow: hidden;
}
button {
  width: 100px;
  height: 50px;
  background-color: aliceblue;
  color: #555;
  font-weight: bold;
  border: none;
  cursor: pointer;
}
button.active {
  color: rgb(0, 152, 223);
  border-bottom: 2px solid rgb(0, 152, 223);
}
.content {
  margin-top: 40px;
}
</style>