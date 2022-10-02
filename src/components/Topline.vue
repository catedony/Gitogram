<template>
  <ul>
    <li><img src="icons/Home.svg" alt="Home"></li>
    <li><Avatar class="avatar" /></li>
    <li><img src="icons/Logout.svg" alt="Logout"></li>
  </ul>
</template>

<script>
import Avatar from './Avatar.vue'
export default {
  name: 'Topline',
  components: { Avatar }
}
</script>

<style lang="scss" scoped>
ul {
  display: flex;
  place-items: center;
}
li {
  width: 32px;
  height: 32px;
}
li:not(:last-child) {
  margin-right: 10px;
}
</style>
