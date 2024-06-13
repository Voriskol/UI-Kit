<script setup>
defineProps({
  label: {
    type: String,
    default: "Button",
  },
  color: {
    type: String,
    default: "primary",
  },
  rounded: {
    type: Boolean,
    default: false,
  },
  disabled: {
    type: Boolean,
    default: false,
  },
  outlined: {
    type: Boolean,
    required: false,
  },
  icon: {
    type: String,
    required: false,
  },
  size: {
    type: String,
    default: "normal",
  },
});

const emit = defineEmits(["click"]);

function clickOnButton() {
  emit("click");
}
</script>

<template>
  <button
    @click="clickOnButton"
    :class="[
      'btn',
      `btn_${color}`,
      { btn_rounded: rounded },
      { btn_outlined: outlined },
      { btn_icon: icon },
      `btn_${size}`,
    ]"
    :disabled="disabled"
  >
    <span v-if="icon"
      ><font-awesome-icon :icon="`fa-regular fa-${icon}`"
    /></span>
    <span v-else>{{ label }}</span>
  </button>
</template>

<style lang="sass" scoped>
.btn
  margin: 0 10px
  color: #fff
  padding: 0 20px
  height: 40px
  border-radius: 7px
  border: none
  cursor: pointer
  font-size: 15px
  transition: .2s
  &_primary
    background: var(--primary)
    border: 1px solid var(--primary)
    &:enabled:hover
      background: var(--primary-hover)

  &_second
    background: var(--second)
    border: 1px solid var(--second)
    &:enabled:hover
      background: var(--second-hover)

  &_success
    background: var(--success)
    border: 1px solid var(--success)
    &:enabled:hover
      background: var(--success-hover)
  &_info
    background: var(--info)
    border: 1px solid var(--info)
    &:enabled:hover
      background: var(--info-hover)
  &_warning
    background: var(--warning)
    border: 1px solid var(--warning)
    &:enabled:hover
      background: var(--warning-hover)
  &_danger
    background: var(--danger)
    border: 1px solid var(--danger)
    &:enabled:hover
      background: var(--danger-hover)
  &:disabled
    opacity: .6
    cursor: default
  &_rounded
    border-radius: 15px
  &_outlined
    background: transparent
    color: #000
    &:hover
      color: #fff
  &_icon
    padding: 0
    width: 40px
    height: 40px
    border-radius: 50%
  &_small
    height: 32px
    padding: 0 15px
  &_large
    height: 48px
    padding: 0 30px
</style>
