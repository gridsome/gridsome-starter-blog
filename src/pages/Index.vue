<template>
  <Layout>
    
    <Author site-title="Gridome Blog Starter" />
    
    <div class="post bg-highlight" >
      <h2>My mars trip 2030</h2>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur excepturi labore tempore expedita, et iste tenetur suscipit explicabo! Dolores, aperiam non officia eos quod asperiores
      </p>
    </div>

    <div class="post bg-highlight" >
      <h2>Lorem ipsum lol</h2>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur excepturi labore tempore expedita, et iste tenetur suscipit explicabo! Dolores, aperiam non officia eos quod asperiores
      </p>
    </div>

    <div class="post bg-highlight">
      <h2>Vue all the things</h2>

      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur excepturi labore tempore expedita, et iste tenetur suscipit explicabo! Dolores, aperiam non officia eos quod asperiores
      </p>
    </div>

    <div class="post bg-highlight">
      <h2>Why speed matters</h2>

      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur excepturi labore tempore expedita, et iste tenetur suscipit explicabo! Dolores, aperiam non officia eos quod asperiores
      </p>
    </div>

    <div class="post bg-highlight">
      <h2>A trip to my school</h2>

      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur excepturi labore tempore expedita, et iste tenetur suscipit explicabo! Dolores, aperiam non officia eos quod asperiores
      </p>
    </div>


  </Layout>
</template>

<script>
import Author from '~/components/Author.vue'

export default {
  components: {
    Author
  },
  metaInfo: {
    title: 'Hello, world!'
  }
}
</script>

<style lang="scss">
.post {
  padding: var(--space);
  margin-top: var(--space);
  border-radius: 5px;
  box-shadow: 1px 1px 5px 0 rgba(0,0,0,.02), 1px 1px 15px 0 rgba(0,0,0,.03);
  transition: transform .3s, background-color .3s, box-shadow .6s;
  &:hover {
    transform: translateY(-5px);
    box-shadow: 1px 10px 30px 0 rgba(0,0,0,.1);
  }
  img {
    // Set image widths
    width: calc(100% + var(--space) * 2);
    margin-left: calc(var(--space) * -1);
  }
}
</style>

