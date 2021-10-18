<template>
  <div>
    <h2>Latest Posts</h2>
    <div class="articles">
      <div class="article" v-for="article of articles" :key="article.slug">
        <!--<nuxt-link :to="{name: 'slug', params: { slug: article.slug } }">-->
          <nuxt-link :to="article.slug">
          <h3>{{article.title}}</h3>
          <p>{{article.description}}</p>
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const articles = await $content('blog', params.slug)
      .only(['title', 'description', 'slug'])
      .sortBy('createdAt', 'asc')
      .fetch()
    return { articles }
  }
}
</script>
