<template>
  <ul class="molecule-sns-link-list">
    <li v-for="item in sns" :key="item.link">
      <sns-link :sns-link="item.link" :img-source="item.imgSource"></sns-link>
    </li>
  </ul>
</template>

<script lang="ts">
import { reactive } from "@vue/reactivity"
import snsLink from "../atoms/snsLink.vue"
export default ({
  name: "snsLinkList",
  components: {
    snsLink,
  },
  setup() {
    const sns = reactive({
      linkedin: {
        link: "https://www.linkedin.com/in/nguyen-thi-hoang-anh-b7688a193/",
        imgSource: require("@/assets/image/sns/icons8-linkedin-circled-50.png")
      },
      github: {
        link: "https://github.com/Crowniizuma",
        imgSource: require("@/assets/image/sns/icons8-github-48.png")
      },
      mail: {
        link: "mailto: nthoanganh10997@gmail.com",
        imgSource: require("@/assets/image/sns/icons8-mail-50.png")
      }
    })
    return {sns};
  },
})
</script>

<style lang="scss">
.molecule-sns-link-list {
  display: flex;
  flex-direction: row;
  column-gap: calc((30/1366)*100vw);
  justify-content: flex-start;
  list-style: none;
}
</style>
