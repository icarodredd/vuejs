<script setup lang="ts">
import { computed, ref } from 'vue'

const one = 1
const someHtml = "<span style='color: red'>This should be red.</span>"
const someClass = 'someClass'
const buttonIsDisabled = true
const count = ref(1)
const isActive = true

const multipleAttributes = {
  id: 'randomId',
  style: 'background-color:green',
}

const author = ref({
  name: 'John Doe',
  books: [
    'Vue 2 - Advanced Guide',
    'Vue 3 - Basic Guide',
    'Vue 4 - The Mystery',
  ],
})

const getFirstBook = computed(() => author.value.books[0])

function onSubmit() {
  console.log('submitted!')
}
</script>

<template>
  <main>
    <p>hello world from vue!</p>
    <p>this is a number: {{ one }}</p>
    <p>someHtml: <span v-html="someHtml"></span></p>
    <p :class="someClass">My class is: {{ someClass }}</p>
    <button :disabled="buttonIsDisabled">Some Button</button>
    <button v-bind="multipleAttributes">
      Button w/ many multiple attributes
    </button>
    <button @click="console.log(1)">Log</button>
    <form @submit.prevent="onSubmit">
      <button type="submit">Submit</button>
    </form>
    <button @click="count++">Click to increment: {{ count }}</button>
    <p>{{ getFirstBook }}</p>
    <p :class="{ active: isActive }"></p>
  </main>
</template>

<style scoped>
main {
  border: dashed white;
  padding: 20px;
}
</style>
