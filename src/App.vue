<script setup>
import { ref } from 'vue';


const selected = ref('請選擇')

const fruits = ref([
  { text: '蘋果', value: 'apple' },
  { text: '香蕉', value: 'banana' },
  { text: '西瓜', value: 'watermelon' }
])



</script>

<template>
  <div>
    請選擇
    <select v-model="selected">
      <option v-for="(option) in fruits" :value="option.value">
        {{ option.text }}
      </option>
    </select>


    <div>被選擇的是：{{ selected }}</div>
  </div>
</template>

<style lang="scss" scoped></style>