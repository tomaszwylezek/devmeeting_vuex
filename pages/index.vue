<template>
  <div>
    <div class="section">
      <main class="container">
        <div class="columns is-multiline">
          <div
            v-for="article in articles"
            :key="article.id"
            class="column is-3"
          >
            <Card :article="article" />
          </div>
        </div>
      </main>
    </div>
  </div>
</template>

<script>
import Card from '~/components/homepage/Card'
export default {
  name: 'HomePage',

  components: {
    Card
  },
  data: () => ({
    articles: [
      {
        id: 'article1',
        slug: 'wstep-do-nuxt-czesc-1',
        imgURL: 'https://nuxtjs.org/logos/nuxt-icon-white.png',
        uploadAt: '2020-02-20',
        author: 'kfras',
        title: 'Wstep do nuxt czesc 1',
        desc: 'To pierwszy artykuł z serii artykułów'
      },
      {
        id: 'article2',
        slug: 'wstep-do-nuxt-czesc-2',
        imgURL: 'https://nuxtjs.org/logos/nuxt-icon-white.png',
        uploadAt: '2020-02-20',
        author: 'kfras',
        title: 'Wstep do nuxt czesc 2',
        desc: 'To drugi artykuł z serii artykułów'
      }
    ]
  })
}
</script>
