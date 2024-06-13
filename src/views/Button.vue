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
    <ElemButton label="Primary" color="primary" rounded />
    <ElemButton label="Secondary" color="second" rounded />
    <ElemButton label="Success" color="success" rounded />
    <ElemButton label="Info" color="info" rounded />
    <ElemButton label="Warning" color="warning" rounded />
    <ElemButton label="Danger" color="danger" rounded />
  </div>
  <h2 class="heading-2">Disabled</h2>
  <div class="line">
    <ElemButton label="Primary" color="primary" disabled />
    <ElemButton label="Secondary" color="second" disabled />
    <ElemButton label="Success" color="success" disabled />
    <ElemButton label="Info" color="info" disabled />
    <ElemButton label="Warning" color="warning" disabled />
    <ElemButton label="Danger" color="danger" disabled />
  </div>
  <h2 class="heading-2">Outlined</h2>
  <div class="line">
    <ElemButton label="Primary" color="primary" outlined />
    <ElemButton label="Secondary" color="second" outlined />
    <ElemButton label="Success" color="success" outlined />
    <ElemButton label="Info" color="info" outlined />
    <ElemButton label="Warning" color="warning" outlined />
    <ElemButton label="Danger" color="danger" outlined />
  </div>
  <h2 class="heading-2">Icon</h2>
  <div class="line">
    <ElemButton color="primary" icon="heart" outlined />
    <ElemButton color="second" icon="hand" />
    <ElemButton color="success" icon="address-book" outlined />
    <ElemButton color="info" icon="credit-card" />
    <ElemButton color="warning" icon="lemon" outlined />
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

<style lang="sass">
@import '@/styles/global.sass'
</style>
