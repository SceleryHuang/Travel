<template>
  <transition name ="haha">
    <slot></slot>
  </transition>
</template>

<script>
export default {
  name: 'FadeAnimation'
}
</script>

<style lang = "stylus" scoped>
  .haha-enter, .haha-leave-to
    opacity: 0
  .haha-leave-active, .haha-enter-active
    transition: opacity 2s
</style>
