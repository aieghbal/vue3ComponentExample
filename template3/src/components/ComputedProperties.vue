<script setup>
import { reactive, computed } from 'vue'

const author = reactive({
  name: 'John Doe',
  books: [
    'Vue 2 - Advanced Guide',
    'Vue 3 - Basic Guide',
    'Vue 4 - The Mystery'
  ]
})
const now = computed(() => Date.now())
// a computed ref
const publishedBooksMessage = computed(() => {
  return author.books.length > 0 ? 'Yes' : 'No'
})
</script>

<template>
	<p>{{ now }}</p>
  <p>Has published books:</p>
  <span>{{ publishedBooksMessage }}</span>
  {{ author.books }}
</template>