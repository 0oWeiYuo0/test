<script setup>
defineProps(['title'])
defineEmits(['remove'])

</script>

<template>
  <div>
    <li>
      {{ title }}
      <button @click="$emit('remove')">刪除</button>
    </li>
  </div>
</template>

<style lang="scss" scoped></style>