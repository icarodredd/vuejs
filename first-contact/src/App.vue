<script setup lang="ts">
const one = 1
const someHtml = "<span style='color: red'>This should be red.</span>"
const someClass = 'someClass'
const buttonIsDisabled = true
</script>

<template>
  <main>
    <p>hello world from vue!</p>
    <p>this is a number: {{ one }}</p>
    <p>someHtml: <span v-html="someHtml"></span></p>
    <p :class="someClass">My class is: {{ someClass }}</p>
    <button :disabled="buttonIsDisabled">Some Button</button>
  </main>
</template>

<style scoped>
main {
  border: dashed white;
  padding: 20px;
}
</style>
