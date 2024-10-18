<script setup lang="ts">
const one = 1
const someHtml = "<span style='color: red'>This should be red.</span>"
const someClass = 'someClass'
</script>

<template>
  <main>
    <p>hello world from vue!</p>
    <p>this is a number: {{ one }}</p>
    <p>someHtml: <span v-html="someHtml"></span></p>
    <p :id="someClass">My class is: {{ someClass }}</p>
  </main>
</template>

<style scoped>
main {
  border: dashed white;
  padding: 20px;
}
</style>
