<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div>
    <main>
      <div class="text-top">Vídeos novos toda <b>quinta</b> às <b>20hs</b></div>
      <a href="https://youtube.com/wdevoficial" target="_blank">
        <img src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/subscribe.svg" alt="Inscreva-se" id="subscribe">
      </a>
      <div class="text-button">youtube.com/wdevoficial</div>
    </main>
  </div>
</template>

<script>
  export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Home'
  }
</script>

<style scoped>
  main {
    background-color: var(--color-background-home);
    justify-content: center;
    align-items: center;
  }

  .text-top {
    color: var(--color-text-light);
    font-size: 22px;
    margin-bottom: 20px;
  }

  #subscribe {
    width: 340px;
  }

  .text-button {
    color: var(--color-text-light);
    font-size: 18px;
    margin-top: 20px;
  }

  @media (min-width: 700px) {
    #subscribe {
      width: 370px;
    }
  }
</style>