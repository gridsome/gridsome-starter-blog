<template>
	<div class="post-card content-box">
		<h2 v-html="post.title" />
		<p v-html="post.excerpt" />
    <PostMeta :post="post" />
		<g-link class="post-card__link" :to="post.path">Link</g-link>
	</div>
</template>

<script>
import PostMeta from '~/components/PostMeta'
export default {
  components: {
    PostMeta
  },
	props: ['post'],
}
</script>

<style lang="scss">
.post-card {
  margin-bottom: var(--space);
  position: relative;

  &:hover {
  	transform: translateY(-5px);
  	box-shadow: 1px 10px 30px 0 rgba(0,0,0,.1);
  }

  &__link {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    opacity: 0.0;
    overflow: hidden;
    text-indent: -9999px;
    z-index: 0;
  }
}
</style>