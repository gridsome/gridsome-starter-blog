<template>
	<div class="author">
		<g-image class="author__image" src="~/assets/images/author.jpg" width="240" height="240" blur="5" />
		<h1 v-if="siteTitle" class="author__site-title">{{ siteTitle }}</h1>
		<p class="author__intro">A minimalistic and simple blog starter for Gridsome that uses Markdown for content.</p>
		<p class="author__links">
			<a href="#">Twitter</a>
			<a href="#">GitHub</a>
		</p>
	</div>
</template>

<script>
export default {
	props: ['siteTitle']
}
</script>

<style lang="scss">
.author {
	margin: 0 auto;
	max-width: 400px;
	text-align: center;
	padding: calc(var(--space) / 2) 0;

	&__image {
		border-radius: 100%;
		width: 120px;
		height: 120px;
		margin-bottom: 1em;
	}

	&__intro {
		opacity: .8;
	}

	&__site-title {
		font-size: 1.5em;
	}

	&__links {
		margin-top: -.5em;
		a {
			margin: 0 .5em;
		}
	}
}
</style>