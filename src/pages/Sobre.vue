<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <main>
    <section class="container">
      <h1>Sobre</h1>
    </section>
    <div class="about" v-html="about"></div>
  </main>
</template>

<script>
  import api from '@/services/api';

  export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Sobre',
    data() {
      return {
        about: ''
      }
    },
    mounted() {
      api.get('/about.json').then(response => {
        this.about = response.data.about;
      });
    }
  }
</script>

<style scoped>
  main {
    align-items: center;
  }

  .about {
    margin-bottom: 40px;
    color: var(--color-text-dark);
  }
</style>
