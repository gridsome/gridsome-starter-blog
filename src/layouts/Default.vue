<template>
  <div id="app">

    <header class="header">
      <div class="header__left">
        <g-link v-if="$route.params.slug" class="logo" to="/">
          <span class="logo__text">Gridsome Blog Starter</span>
        </g-link>
      </div>
      <div class="header__right">        
        <ToggleTheme />
      </div>
    </header>

    <main class="main">
      <slot/>
    </main>

    <footer class="footer">
      Copyright © {{ new Date().getFullYear() }}. Powered by <a href="//gridsome.org"> Gridsome </a>
    </footer>

  </div>
</template>

<script>
import ToggleTheme from '~/components/ToggleTheme.vue'

export default {
  components: {
    ToggleTheme
  }
}
</script>

<style lang="scss">
.logo {
  text-decoration: none;
  color: var(--body-color)!important;
  font-size: .9em;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  min-height: 60px;
  padding: 0 calc(var(--space) / 2);
  top:0;
  z-index: 10;

  &__left,
  &__right {
    display: flex;
    align-items: center;
  }

  @media screen and (min-width: 1200px) {
    //Make header sticky for large screens
    position: sticky;
  }
}

.main {
  max-width: var(--container-width);
  margin: 0 auto;
  padding: 3.33vw 15px 0;
}

.footer {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: calc(var(--space) / 2);
  text-align: center;
  font-size: .8em;

  a {
    color: currentColor;
    margin: 0 .35em;
  }
}
</style>
