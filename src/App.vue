<script setup>
import { ref } from "vue";

const num = ref(0)

function warn(message, event) {
  // 這裡可以訪問原生事件
  if (event) {
    event.preventDefault()
  }
  alert(message)
}

const handleKeyup = (event) => {
  if (event.altKey && event.key === 'Enter') {
    clear();
  }
};

const clear = () => {
  console.log('Clearing the input!');
};

</script>

<template>
  <div>
    <input type="text" @keyup="handleKeyup">
  </div>
</template>

<style lang="scss" scoped></style>