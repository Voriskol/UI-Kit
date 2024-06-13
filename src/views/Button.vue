<script setup>
import ElemButton from "@/components/ElemButton.vue";

const eventForButton = () => {
  alert("Clicked");
};
</script>

<template>
  <h1 class="heading-1">Button</h1>
  <h2 class="heading-2">Colors</h2>
  <div class="line">
    <ElemButton label="Primary" color="primary" />
    <ElemButton label="Secondary" color="second" />
    <ElemButton label="Success" color="success" />
    <ElemButton label="Info" color="info" />
    <ElemButton label="Warning" color="warning" />
    <ElemButton label="Danger" color="danger" />
  </div>
  <h2 class="heading-2">Rounded</h2>
  <div class="line">
    <ElemButton label="Primary" color="primary" :rounded="true" />
    <ElemButton label="Secondary" color="second" :rounded="true" />
    <ElemButton label="Success" color="success" :rounded="true" />
    <ElemButton label="Info" color="info" :rounded="true" />
    <ElemButton label="Warning" color="warning" :rounded="true" />
    <ElemButton label="Danger" color="danger" :rounded="true" />
  </div>
  <h2 class="heading-2">Disabled</h2>
  <div class="line">
    <ElemButton label="Primary" color="primary" :disabled="true" />
    <ElemButton label="Secondary" color="second" :disabled="true" />
    <ElemButton label="Success" color="success" :disabled="true" />
    <ElemButton label="Info" color="info" :disabled="true" />
    <ElemButton label="Warning" color="warning" :disabled="true" />
    <ElemButton label="Danger" color="danger" :disabled="true" />
  </div>
  <h2 class="heading-2">Outlined</h2>
  <div class="line">
    <ElemButton label="Primary" color="primary" :outlined="true" />
    <ElemButton label="Secondary" color="second" :outlined="true" />
    <ElemButton label="Success" color="success" :outlined="true" />
    <ElemButton label="Info" color="info" :outlined="true" />
    <ElemButton label="Warning" color="warning" :outlined="true" />
    <ElemButton label="Danger" color="danger" :outlined="true" />
  </div>
  <h2 class="heading-2">Icon</h2>
  <div class="line">
    <ElemButton color="primary" icon="heart" :outlined="true" />
    <ElemButton color="second" icon="hand" />
    <ElemButton color="success" icon="address-book" :outlined="true" />
    <ElemButton color="info" icon="credit-card" />
    <ElemButton color="warning" icon="lemon" :outlined="true" />
    <ElemButton color="danger" icon="hourglass" />
  </div>
  <h2 class="heading-2">Size</h2>
  <div class="line">
    <ElemButton label="Small" color="primary" size="small" />
    <ElemButton label="Normal" color="primary" />
    <ElemButton label="Large" color="primary" size="large" />
  </div>
  <h2 class="heading-2">Event</h2>
  <div class="line">
    <ElemButton label="@click" color="second" @click="eventForButton" />
  </div>
</template>

<style lang="sass" scoped>
.line
  display: flex
  flex-wrap: wrap
  margin-bottom: 20px
</style>
