<template>
  <router-link :to="link" class="atom-nav-link">{{ label }}</router-link>
</template>

<script lang="ts">
export default ({
  name: "navLink",
  props: {
    label: {
      type: String,
      required: true,
    },
    link: {
      type: String,
      requied: true,
      default: '/'
    }
  }
})
</script>

<style lang="scss">
.atom-nav-link {
  color: #000;
  font-size: 20px;
  text-decoration: none;
  &:hover {
    color: rgb(145, 145, 145);
  };
}
</style>