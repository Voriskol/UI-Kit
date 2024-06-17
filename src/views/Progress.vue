<script setup>
import { ref } from "vue";
import ProgressBar from "@/components/Progress/ProgressBar.vue";
import ProgressCircle from "@/components/Progress/ProgressCircle.vue";
import Button from "@/components/ElemButton.vue";

const percentBar = ref(40);
const percentCircle = ref(60);

function addPercentBar() {
  if (percentBar.value < 100) {
    percentBar.value += 10;
  } else {
    percentBar.value = 0;
  }
  return percentBar;
}

function addPercentCircle() {
  if (percentCircle.value < 100) {
    percentCircle.value += 10;
  } else {
    percentCircle.value = 0;
  }
  return percentCircle;
}
</script>

<template>
  <h1 class="heading-1">Progress</h1>
  <h2 class="heading-2">Progress bar</h2>
  <div class="line line_block">
    <ProgressBar maxWidth="600px" :percent="percentBar" color="danger" />
    <Button label="Add 10%" @click="addPercentBar" />
  </div>
  <h2 class="heading-2">Progress circle</h2>
  <div class="line line_block">
    <ProgressCircle :percent="percentCircle" color="success" />
    <Button label="Add 10%" @click="addPercentCircle" />
  </div>
</template>
