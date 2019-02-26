<template>
	<div class="post-card bg-highlight">
		<h2 v-html="post.title" />
		{{ post }}
		<p>
		  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur excepturi labore tempore expedita, et iste tenetur suscipit explicabo! Dolores, aperiam non officia eos quod asperiores
		</p>
		<g-link class="post-card__link" :to="post.path">Link</g-link>
	</div>
</template>

<script>
export default {
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