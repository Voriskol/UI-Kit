<script setup>
import { ref, reactive } from "vue";
import ElemCheckbox from "@/components/Checkbox/ElemCheckbox.vue";

const checkboxActive = ref(true);
const checkboxDisabled = ref(true);
const checkboxDisabledChecked = ref(true);
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
</template>
