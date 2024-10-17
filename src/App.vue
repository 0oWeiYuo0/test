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

</script>

<template>
  <div>
    <!-- 單擊事件將停止傳遞 -->
    <a @click.stop="doThis"></a>

    <!-- 提交事件將不再重新加載頁面 -->
    <form @submit.prevent="onSubmit"></form>

    <!-- 修飾語可以使用鏈式書寫 -->
    <a @click.stop.prevent="doThat"></a>

    <!-- 也可以只有修飾符 -->
    <form @submit.prevent></form>

    <!-- 僅當 event.target 是元素本身時才會觸發事件處理器 -->
    <!-- 例如：事件處理器不來自子元素 -->
    <div @click.self="doThat">...</div>
  </div>
</template>

<style lang="scss" scoped></style>