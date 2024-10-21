<script setup lang="ts">
import { ref } from 'vue'

const one = 1
const someHtml = "<span style='color: red'>This should be red.</span>"
const someClass = 'someClass'
const buttonIsDisabled = true
const count = ref(1)

const multipleAttributes = {
  id: 'randomId',
  style: 'background-color:green',
}

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
  </main>
</template>

<style scoped>
main {
  border: dashed white;
  padding: 20px;
}
</style>
