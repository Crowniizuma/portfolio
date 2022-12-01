<template>
  <Header></Header>
  <router-view/>
</template>


<script lang="ts">
import Header from "./components/organisms/header.vue"
export default ({
  components: {
    Header
  },
  setup() {
  },
})
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Rubik&display=swap');
#app {
  font-family: 'Rubik', sans-serif;
}
</style>

