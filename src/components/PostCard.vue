<template>
	<div class="post-card content-box">
    <div class="post-card__header">
      <!-- Add anything here. Like a featured image -->
    </div>
		<h2 class="post-card__title" v-html="post.title" />
		<p class="post-card__excerpt" v-html="post.excerpt" />
    <PostMeta class="post-card__meta" :post="post" />
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

  &__header {
    width: calc(100% + var(--space) * 2);
    margin-left: calc(var(--space) * -1);
    margin-top: calc(var(--space) * -1);
    margin-bottom: calc(var(--space) / 2);
    
    &:empty {
      display: none;
    }
  }

  &__title {
    margin-top: 0;
  }

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