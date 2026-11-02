<script setup>
import { ref } from 'vue';

const pro = ref(false);
const set = ref(false);
const noti = ref(false);

const togglePro = () => {
    pro.value = true;
    set.value = false;
    noti.value = false;
}
const toggleSet = () => {
    pro.value = false;
    set.value = true;
    noti.value = false;
}
const toggleNoti = () => {
    pro.value = false;
    set.value = false; 
    noti.value = true;
}
</script>

<template>
  <div class="btn">
    <button :class="{'btn-pro': pro === true}" @click="togglePro">프로필</button>
    <button :class="{'btn-set': set === true}" @click="toggleSet">설정</button>
    <button :class="{'btn-noti': noti === true}" @click="toggleNoti">게시판</button>
  </div>
  <br><br>
<p v-if="pro">프로필 페이지입니다.</p>
<p v-if="set">설정 페이지입니다.</p>
<p v-if="noti">게시판 페이지입니다.</p>
</template>

<style>
  .btn{
    display: flex;
    margin: 20px auto;
    border-radius: 10px;
    overflow: hidden;
  }
  button{
    width: 100px;
    height: 50px;
    background-color: aliceblue;
    color: #555;
    font-weight: bold;
    border: none;
  }
  .btn-pro, .btn-set, .btn-noti {
    color: rgb(0, 152, 223);
    border-bottom: 2px solid rgb(0, 152, 223);
  }
</style>
