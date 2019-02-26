<template>
	<Layout>
		<div style="text-align: center">
				<g-link to="/">Gridsome Blog Starter</g-link>
			<h1> {{ $page.post.title }} </h1>
		</div>
		
		<div class="post bg-highlight">
			<div v-html="$page.post.content" />
		</div>

		<Author />
	</Layout>
</template>

<script>
import Author from '~/components/Author.vue'
export default {
	components: {
		Author
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
.post {
	img {
		width: calc(100% + var(--space) * 2);
		margin-left: calc(var(--space) * -1);
	}
	pre {
		font-size: .85em;
		background-color: var(--bg-code);
		color: var(--body-color);
		text-shadow: none;
		margin-bottom: 2em;
	}
	code {
		background-color: var(--bg-code)!important;
		color: var(--body-color);
		text-shadow: none;
	}
}
</style>