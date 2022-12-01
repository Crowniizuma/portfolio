<template>
  <ul class="molecule-nav-link-list">
    <li v-for="route in routes" :key="route.link">
      <nav-link :link="route.link" 
                :label="route.label" >
      </nav-link>
    </li>
  </ul>
</template>

<script lang="ts">
import { reactive } from "@vue/reactivity"
import navLink from "../atoms/navLink.vue";
export default ({
  name: "navLinkList",
  components: {
    navLink
  },
  setup() {
    const routes = reactive({
      home : {
        link: "/",
        label: "home"
      },
      about : {
        link: "/about",
        label: "about"
      },
      projects : {
        link: "/projects",
        label: "projects"
      },
      blog : {
        link: "/blog",
        label: "blog"
      },
    })
    return {routes}
  },
})
</script>

<style lang="scss">
.molecule-nav-link-list {
  display: flex;
  column-gap: calc((50/1366)*100vw);
  justify-content: right;
  align-items: center;
  list-style: none;
}
</style>