<script setup>
import { ref } from "vue";
import ElemRadiobutton from "@/components/ElemRadiobutton.vue";

const footballClubs = ref([
  {
    name: "Real Madrid",
    id: "f1",
  },
  {
    name: "Barcelona",
    id: "f2",
  },
  {
    name: "Bayern Munich",
    id: "f3",
  },
  {
    name: "Paris Saint-Germain",
    id: "f4",
  },
]);

const selectedClub = ref("");

const disabledRadio = ref(true);

const disabledRadioChecked = ref(true);
</script>

<template>
  <h1 class="heading-1">Radiobutton</h1>
  <h2 class="heading-2">Basic</h2>
  <div class="line line_block">
    <p>Selected Club: {{ selectedClub }}</p>
    <div v-for="club in footballClubs" :key="club.id">
      <ElemRadiobutton
        :value="club.name"
        :label="club.name"
        :id="club.id"
        name="club"
        v-model:checkedValue="selectedClub"
      />
    </div>
  </div>
  <h2 class="heading-2">Disabled</h2>
  <div class="line">
    <div>
      <ElemRadiobutton
        value="Radiobutton Disabled"
        label="Radiobutton Disabled"
        id="RadiobuttonDisabled"
        name="RadiobuttonDisabled"
        :disabled="disabledRadio"
        v-model:checkedValue="disabledRadioChecked"
      />
    </div>
  </div>
</template>
