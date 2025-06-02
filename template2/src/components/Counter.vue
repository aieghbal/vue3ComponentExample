<template>
  <div class="counter-box">
    <h2>شمارنده</h2>
    <p>عدد فعلی: {{ count }}</p>
    <button @click="increment">افزایش</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const count = ref(0)

const increment = () => {
  count.value++
}
</script>

<style scoped>
.counter-box {
  text-align: center;
  margin: 20px auto;
}

button {
  padding: 8px 16px;
  font-size: 16px;
  cursor: pointer;
}
</style>
