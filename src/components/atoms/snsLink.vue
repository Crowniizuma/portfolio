<template>
  <a :href="snsLink" class="sns-link" target="_blank">
    <img :src="imgSource"/>
  </a>
</template>

<script lang="ts">

export default ({
  name: "snsLink",
  setup() {
    
  },
  props: {
    snsLink: {
      type: String,
      required: true
    },
    imgSource: {
      type: String,
      required: true
    }
  }
})
</script>

<style lang="scss">
.sns-link {
  

  img{
    width: 40px;
    height: 40px;
  }
}
</style>