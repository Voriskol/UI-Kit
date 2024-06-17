<script setup>
import LayoutHeader from "@/components/Layout/Header.vue";
import LayoutSideBar from "@/components/Layout/SideBar.vue";
import { ref } from "vue";

const isOpenMenu = ref(false);

function toggleMenu() {
  isOpenMenu.value = !isOpenMenu.value;
}
</script>

<template>
  <div class="container">
    <div class="sidebar-toggle" @click="toggleMenu">&#5125;</div>
    <LayoutHeader />
    <LayoutSideBar :openSideBar="isOpenMenu" />
    <div :class="['content', { content_full: !isOpenMenu }]">
      <RouterView />
    </div>
  </div>
</template>

<style lang="sass">
@import './styles/global.sass'

.content
  max-width: 1400px
  margin-left: 250px
  padding-left: 20px
  padding-top: 62px
  transition: .2s
  &_full
    margin-left: 0


.sidebar-toggle
  position: fixed
  left: 0
  width: 15px
  background: var(--primary)
  height: 100%
  top: 62px
  z-index: 1
  cursor: pointer
  color: #fff
  display: flex
  align-items: center
  justify-content: center


@media screen and (max-width: 1023px)
  .content
    margin-left: 0
</style>
