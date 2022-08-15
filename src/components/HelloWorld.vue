<script setup lang="ts">
import { storeToRefs } from "pinia";
import { mainStore } from "../store";
const store = mainStore();
let { msg } = storeToRefs(store);
const changeMsg = function () {
  store.msg = "123";
};
</script>

<template>
  <button @click="changeMsg">按钮</button>
  <h1>{{ msg }}</h1>
</template>

<style scoped></style>
