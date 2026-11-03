<script setup>
import { defineProps } from 'vue';
const props = defineProps({
  'item' : Object,
  'str' : String
});
</script>

<template>
  <h2>Child</h2>
  <p>{{ props.item.name }}</p>
</template>

<style>

</style>