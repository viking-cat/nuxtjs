<template>
  <article>
    <nuxt-content :document="article" />
  </article>
</template>

<style>
</style>

<script>
export default {
  async asyncData ({ $content, params }) {
    const article = await $content('blog', params.slug).fetch()
    return { article }
  }
}
</script>
