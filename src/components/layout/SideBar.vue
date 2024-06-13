<script setup>
import { ref, reactive } from "vue";

defineProps({
  openSideBar: {
    type: Boolean,
    required: true,
  },
});

const links = reactive([
  {
    name: "Typography",
    href: "/typography",
  },
  {
    name: "Button",
    href: "/button",
  },
  {
    name: "Checkbox",
    href: "/checkbox",
  }
]);
</script>

<template>
  <div :class="['sidebar', { sidebar_isopen: openSideBar }]">
    <router-link
      class="sidebar__link"
      v-for="link in links"
      :key="link.name"
      :to="link.href"
      >{{ link.name }}</router-link
    >
  </div>
</template>

<style lang="sass" scoped>
.sidebar
  left: 0
  top: 62px
  height: 100%
  background: #fff
  position: fixed
  width: 250px
  padding: 20px
  transition: 0.2s
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.07)
  transform: translateX(-250px)
  &_isopen
    transform: translateX(0)
  &__link
    display: block
    border-radius: 12px
    padding: 10px
    border: 2px solid #fff
    transition: 0.2s
    font-weight: bold
    margin-bottom: 10px
    &:hover
      border-color: var(--primary)
</style>
