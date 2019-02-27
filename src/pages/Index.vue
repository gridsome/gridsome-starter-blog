<template>
  <Layout>
    
    <Author :site-title="$static.metaData.siteName" />
    
    <div class="posts">
      <PostCard v-for="edge in $page.posts.edges" :key="edge.node.id" :post="edge.node"/>
    </div>

  </Layout>
</template>

<static-query>
query {
  metaData {
    siteName
  }
}
</static-query>

<page-query>
{
  posts: allPost {
    edges {
      node {
        id
        title
        path
        date (format: "D. MMMM YYYY")
        timeToRead
        excerpt
      }
    }
  }
}
</page-query>

<script>
import Author from '~/components/Author.vue'
import PostCard from '~/components/PostCard.vue'

export default {
  components: {
    Author,
    PostCard
  },
  metaInfo: {
    title: 'Hello, world!'
  }
}
</script>

<style lang="scss">

</style>

