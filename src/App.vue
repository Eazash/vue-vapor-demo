<script setup lang="ts">
import { shallowReactive } from "vue";
const appState = shallowReactive({
  count: 0,
  hidden: {
    count: 0,
  },
});
function inc() {
  appState.count++;
}
function incHidden() {
  appState.hidden.count++;
}
</script>

<template>
  <h1>Hello, Vue Vapor!</h1>
  <p>Count: {{ appState.count }}, Hidden Count: {{ appState.hidden.count }}</p>
  <button @click="inc">increase</button>
  <button @click="incHidden">increase</button>
</template>
