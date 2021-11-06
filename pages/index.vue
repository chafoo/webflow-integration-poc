<template>
  <div class="content-container" v-html="html"/>
</template>

<script>
import Vue from 'vue'

export default Vue.extend({
  async asyncData({ $axios }) {
    const response = await $axios.get("https://blog.mycuraya.com/")
    let html = response?.data.toString()

    html = html.replace(
      `Willst Du ein Teil der Bewegung werden?`, 
      `<a id="custom-cta" href="#call-event">Custom Internal Cta</a>`
    )

    // console.log(#html", html)

    return {
      html
    }
  }
})
</script>
