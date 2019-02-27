<template>
	<Layout>
		<div class="post-title">
			<h1 class="post-title__text"> {{ $page.post.title }} </h1>
			<PostMeta :post="$page.post" />
		</div>
		
		<div class="post bg-highlight">
			<div class="post__header">
				<!-- Add anything here. Like a featured image -->
			</div>
			<div class="post__content" v-html="$page.post.content" />
			<div class="post__footer">
				<!-- Add anything here -->
			</div>
		</div>

		<div class="post-comments">
			<!-- Add comment widgets here -->
		</div>

		<Author />
	</Layout>
</template>

<script>
import PostMeta from '~/components/PostMeta'
import Author from '~/components/Author.vue'

export default {
	components: {
		Author,
		PostMeta
	}
}
</script>

<page-query>
query Post ($path: String!) {
  post: post (path: $path) {
    title
    content
  }
}
</page-query>

<style lang="scss">

.post-title {
	padding: calc(var(--space) / 2) 0;
	text-align: center;
}

.post {

	&__header {
		width: calc(100% + var(--space) * 2);
		margin-left: calc(var(--space) * -1);
		margin-top: calc(var(--space) * -1);
		
		&:empty {
			display: none;
		}
	}

	img {
		width: calc(100% + var(--space) * 2);
		margin-left: calc(var(--space) * -1);
	}

	pre {
		width: calc(100% + var(--space) * 2);
		margin-left: calc(var(--space) * -1);
		padding: calc(var(--space) / 2);
		font-size: .85em;
		background-color: var(--bg-code);
		color: var(--body-color);
		text-shadow: none;
		margin-bottom: 2em;
		border-top: 1px solid rgba(0,0,0,.03);
		border-bottom: 1px solid rgba(0,0,0,.03);
	}

	code {
		background-color: var(--bg-code)!important;
		color: var(--body-color);
		text-shadow: none;
	}
}

.post-comments {
	padding: calc(var(--space) / 2);
	&:empty {
		display: none;
	}
}
</style>