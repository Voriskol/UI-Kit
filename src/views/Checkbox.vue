<script setup>
import { ref } from "vue";
import ElemCheckbox from "@/components/Checkbox/ElemCheckbox.vue";
import CheckboxGroup from "@/components/Checkbox/CheckboxGroup.vue";

const checkboxActive = ref(true);
const checkboxDisabled = ref(true);
const checkboxDisabledChecked = ref(true);

const listOfHeroes = ref([
  {
    name: "Superman",
    id: "h1",
  },
  {
    name: "Batman",
    id: "h2",
  },
  {
    name: "Spiderman",
    id: "h3",
  },
  {
    name: "Hulk",
    id: "h4",
  },
]);
const selectedHeroes = ref(["h1", "h3"]);

const switchProfessional = ref(false);
</script>

<template>
  <h1 class="heading-1">Checkbox</h1>
  <h2 class="heading-2">Checkbox Active</h2>
  {{ checkboxActive }}
  <div class="line">
    <ElemCheckbox
      label="Checkbox Active"
      id="checkboxActive"
      name="checkboxActive"
      value="I am active"
      v-model:checked="checkboxActive"
    />
  </div>

  <h2 class="heading-2">Checkbox Disabled</h2>
  <div class="line">
    <ElemCheckbox
      label="Checkbox Disabled"
      id="checkboxDisabled"
      name="checkboxDisabled"
      value="I am disabled"
      :disabled="checkboxDisabled"
      v-model:checked="checkboxDisabledChecked"
    />
  </div>
  <h2 class="heading-2">Checkbox Group</h2>
  <div class="line line_block">
    <p>Selected heroes: {{ selectedHeroes }}</p>
    <CheckboxGroup
      v-model:value="selectedHeroes"
      :options="listOfHeroes"
      name="heroes"
    />
  </div>
  <h2 class="heading-2">Switch</h2>
  <p>Switch: {{ switchProfessional }}</p>
  <div class="line">
    <ElemCheckbox
      label="I'm a professional"
      id="switch"
      name="switch"
      value="I am a professional"
      type="switch"
      v-model:checked="switchProfessional"
    />
  </div>
</template>
