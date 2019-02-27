<template>
	<Layout>
		<div class="post-title">
			<h1 class="post-title__text"> {{ $page.post.title }} </h1>
			<PostMeta :post="$page.post" />
		</div>
		
		<div class="post content-box">
			<div class="post__header">
				<g-image v-if="$page.post.poster" :src="$page.post.poster" />
			</div>
			<p v-if="$page.post.excerpt" class="post__excerpt" v-html="$page.post.excerpt" />
			<div class="post__content" v-html="$page.post.content" />
			<div class="post__footer">
				<!-- Add anything here -->
			</div>
		</div>

		<div class="post-comments">
			<!-- Add comment widgets here -->
		</div>

		<Author class="post-author" />
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
    path
    date (format: "D. MMMM YYYY")
    timeToRead
    excerpt
    content
    poster (width: 780, blur: 10)
  }
}
</page-query>

<style lang="scss">
.post-title {
	padding: calc(var(--space) / 2) 0 var(--space);
	text-align: center;
}

.post {

	&__header {
		width: calc(100% + var(--space) * 2);
		margin-left: calc(var(--space) * -1);
		margin-top: calc(var(--space) * -1);
		margin-bottom: calc(var(--space) / 2);
		overflow: hidden;
		border-radius: var(--radius) var(--radius) 0 0;
		
		&:empty {
			display: none;
		}
	}

	&__excerpt {
		font-size: 1.2em;
		color: var(--title-color);
	}

	&__content {
		img {
			width: calc(100% + var(--space) * 2);
			margin-left: calc(var(--space) * -1);
			display: block;
		}
	}
}

.post-comments {
	padding: calc(var(--space) / 2);
	
	&:empty {
		display: none;
	}
}

.post-author {
	margin-top: calc(var(--space) / 2);
}
</style>