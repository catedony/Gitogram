<template>
  <button @click="$emit('toggle')" class="toggler"><slot></slot><span ><img src="icons/Toggler.svg" :class="['toggler__icon', {isOpen: isOpen}]"></span></button>
</template>

<script>
export default {
  name: 'Toggler',
  props: {
    isOpen: {
      type: Boolean,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.toggler {
  background: none;
  border: none;
  padding: 0;
  font-weight: bold;
  &__icon {
    transition: all 200ms;
    margin-left: 5px;
  }
  &__icon.isOpen {
    transform: rotate(180deg)
  }
}
</style>
