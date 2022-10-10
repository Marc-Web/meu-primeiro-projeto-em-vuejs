<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <header>
    <nav class="container">
      <a href="/">
        <img src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/wdev.svg" alt="WDEV" id="logo">
      </a>
      <img src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/menu.svg" alt="Abrir menu" id="menu-button" >
    </nav>
  </header>
</template>

<script>
  export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Header'
  }
</script>

<style scoped>
  header {
    background-color: var(--color-background-nav);
    height: 60px;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  nav {
    display: flex;
    justify-content: space-between;
  }

  #logo {
   width: 130px;
  }

  #menu-button {
   width: 30px;
  }
</style>