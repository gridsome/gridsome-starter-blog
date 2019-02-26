<template>
  <div id="app">

    <header class="header">
      <div class="header__left">
        <!-- add anything here --> 
      </div>
      <div class="header__right">        
        <!-- add anything here -->
        <ToggleTheme />
      </div>
    </header>

    <transition name="slide-up" appear>
      <main class="main">
        <slot/>
      </main>
    </transition>

    <footer class="footer">
      Copyright © {{ new Date().getFullYear() }} 
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
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: sticky;
  top:0;
  z-index: 10;
}

.main {
  max-width: 760px;
  margin: 0 auto;
  padding: 5vw 15px 0;
}

.footer {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: var(--space);
  text-align: center;
}

.slide-up-enter-active {
  transition: opacity .3s, transform .5s;
}

.slide-up-enter {
  opacity: 0;
  transform: translateY(5px);
}
</style>
