<template>
  <div class="header">
    <nav-link-list></nav-link-list>
    <sns-link-list></sns-link-list>
  </div>
</template>

<script lang="ts">
import navLinkList from '../molecules/navLinkList.vue';
import snsLinkList from '../molecules/snsLinkList.vue';
export default ({
  name: "Header",
  components: {
    navLinkList,
    snsLinkList
  },
  setup() {
    
  },
})
</script>

<style lang="scss">
.header {
  display: flex;
  column-gap: calc((50/1366)*100vw);
  justify-content: right;
  width: calc(100vw - 200px);
  padding: 25px 100px;
}
</style>